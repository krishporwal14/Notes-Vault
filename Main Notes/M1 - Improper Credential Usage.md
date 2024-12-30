<center><h1>M1 - Improper Credential Usage</h1></center>

## Metadata
- **Date:** 24/12/2024  
- **Tags:** [[cybersecurity]] [[apphacking]] [[year2024]] [[android]] [[mobile]] [[unauthorized access]]
- **Author/Name:** Krish Porwal

---

## Theory
#### Threat Agents
- Application Specific.
- Exploit hardcoded credentials usage and improper credential usage in mobile applications.
- May include automated attacks using various tools.

#### Attack Methods
- Very easy to exploit.
- Can gain [[unauthorized access]] to sensitive mobile app functions by exploiting vulnerabilities in hardcoded credentials and improper credential.
- Can also misuse credentials, through improperly validated or stored credentials.
- Bypassing the need for legitimate access.

#### Security Weakness
- Occurrence is <u>common</u>.
- <u>Easy</u> to detect.
- Should check the source code to find hardcoded credentials.

#### Impacts
- Both technical and business impact is <u>severe</u>.
- Technical impacts include unauthorized access,  data breaches, loss of user privacy, fraudulent activity, and access to admin functionality.
- Business impacts include reputation damage, information theft, fraud, unauthorized access to data.

#### Who is vulnerable?
Mobile apps with,
- Hardcoded Credentials
- Insecure Credential Transmission (without encryption, etc)
- Insecure Credential Storage
- Weak User Authentication.

#### Prevention
- Avoid using Hardcoded Credentials.
- Properly handle user credentials.
- Encrypt credentials during transmission.
- Instead of storing credentials on the device, use secure, revocable, access tokens.
- Implement Strong User Authentication Protocols.
- Regularly update the API keys or tokens.

---

## Scenarios
![[Pasted image 20241225112545.png]]

---

## Summary
> Mobile applications are vulnerable to improper credential usage if they have hardcoded credentials, insecure credential transmission and storage, and weak user authentication protocol. These type of vulnerabilities are common and easy to exploit. Both technical and business impacts of these vulnerabilities are severe. Use encrypted transmission, API keys or tokens, strong user authentication protocol, and more.

---

## References
[Owasp](https://owasp.org/www-project-mobile-top-10/2023-risks/m1-improper-credential-usage.html)
