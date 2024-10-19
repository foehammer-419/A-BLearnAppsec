# A-BLearnAppsec
Alice And Bob Learn Appsec Notes



### CH1: Security Fundamentals

The CIA Triad
  - Confidentiality, Integrity, Availability
 
    Confidentiality
    - The capability to keep private things private as one chooses
    - AKA: Keeping things safe
   
    Integrity
    - Data is current, correct, and accurate
    - Data should NOT be altered during transmission (what comes in is what comes out)
   
    Availability
    - A device/program is capable of performing its expected functions when it is needed or called upon.
    - Having more robust or resilient systems improves availability
   
Assume Breach
  - The 2 types of companies: Those that have been breached and those who have been, but don't know yet
  - The assume breach concept means preparing and design considerations to ensure that if someone were to gain unapproved access to your data, application, network, etc... it would be difficult to do anything harmful AND you could easily detect/respond to it via monitoring/logging 
  - This can cover everything from personal to professional from 2FA to granular RBAC/document control to Zero Trust to everything in between
  - Another aspect of this can be coordinated disclosure, where vulnerabilties/issues are disclosed after a period of time that allows for patching

Insider Threats
- An Insider Threat is someone who has approved access to systems that negatively impacts one or more of the CIA triad components
- For example an employee improperly using software causing an outage, or someone taking PII/PHI home on a USB drive, etc...

Defense in Depth
- Having multiple layers of security in case one is breached/not enough
- An example of this is from the application level: having secure coding practices, then doing security testing on the coded app, and finally having the application check/sanitize input
- Even documentation, design, firewalls, monitoring, locks/gates, logging, etc... can all be part of defense in depth.
- Oftentimes the hardest part is convincing others that security is important especially in a business sense

Least Privilege
- Giving users exactly how much access/control they need and nothing more
- Oftentimes done in case of a malicious account takeover of a users

Supply Chain Security
- Each item/software package you use to create an item is potentially a vulnerability or risk if it becomes compromised.
- Given that modern apps are often only ~20-40% original code and up to 90% of commercial applications rely on outdated FOSS components (securitymagazine, 2020) these dependencies create downstream issues because if one of them has a security issue, you might now have one too.
- The best way to approach the software supply chain is to use frameworks by well known companies and practice secure coding by regularly using tools against your codebase and updated code.

Security by Obscurity

- Attempting to hide or obfuscate code/other assets as a security measure, this can be helpful as a defense in depth layer

Attack surface reduction

- Every component of an application (buttons, tags, pages, features, etc...) can potentially be exploited so reducing the attack surface means removing anything unecessary.

Hard coding

- Putting values into the code itself rather than getting the values from a DB, user, API, etc... don't expose potentially sensitive values to anyone who might have the source code as it is poor software development practice

Always Verify

- Don't trust anything outside the application, always verify any input/data that comes in from a source (user, DB, API, etc...).  Verify and re-verify don't just trust in the context of the program, state changes and user/application sessions change constantly, verify that those are still valid.

Usable Security

- While it's easier to lock something and throw away the key, there has to be some compromise between the world of security and usability so that users don't constantly try and get around security thus making the application/data less secure.

Factors of Authentication
- Something you have (badge, phone, token, etc...)
- Something you are (fingerprint, facial ID, etc...)
- Something you know (password, pattern, security question)

- Multifactor authenticaion should be the goal, Multifactor authentication combines 2 or more of the above factors (i.e. a password as something you know, and a phone authenticator as something you have) Note: using 2 factors of the same type (i.e. a security question AND a password) does NOT constitute MFA

### Ch2: Security Requirements
  
