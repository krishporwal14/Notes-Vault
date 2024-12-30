<center><h1>M2 - Inadequate Supply Chain Security</h1></center>

## Metadata
- **Date:** 24/12/2024  
- **Tags:** [[cybersecurity]] [[apphacking]] [[year2024]] [[android]] [[mobile]] [[unauthorized access]] [[denial of service]]
- **Author/Name:** Krish Porwal

---

## Theory
#### Threat Agents
- Application Specific.
- Can manipulate application functionalities by exploiting vulnerabilities in mobile app.
- Insertion of malicious code in the codebase or modify the code during the build process to introduce backdoors, spyware, etc.
- Allows the attacker to steal data, spy on users, or take control of the mobile device.
- Can also exploit third-party software libraries, SDKs, vendors, etc.
- Can lead to [[unauthorized access]], [[denial of service]], or complete takeover of the mobile app or device.

#### Attack Methods
- Exploitability is <u>average</u>.
- Insider threat agent or an attacker can inject malicious code during the development phase, then they can compromise the app signing keys or certificates, to sign malicious code as trusted.
- Can also exploit third-party libraries or components used in the app.

#### Security Weakness
- Occurrence is <u>common</u>.
- <u>Difficult</u> to detect.
- Occurs due to lack of secure coding practices, insufficient code reviews and testing.
- Insufficient and insecure app signing process, weakness in third-party software, or exposing sensitive data to [[unauthorized access]].

#### Impacts
- Both technical and business impacts are <u>severe</u>.
- Technical impacts include data breach, malware infection, [[unauthorized access]], system compromise.
- Business impacts include financial losses, reputational damage, legal consequences, supply chain disruption.

#### Who is vulnerable?
Mobile apps with,
- Lack of Security in Third-party Components
- Malicious Insider Threats
- Inadequate Testing and Validation
- Lack of Security Awareness.

#### Prevention
- Implement secure coding practices, code review, and testing.
- Ensure secure app signing.
- Use only trusted and validated third-party libraries or components.
- Establish security controls for app updates, patches, and releases.
- Monitor and detect supply chain security incidents using security testing, scanning, etc.

---

## Scenarios
![[Pasted image 20241225112457.png]]

---

## Summary
> Application specific vulnerability which occurs due to insider threats, lack of code reviews and testing, use of unsafe third-party components,, etc. Occurs commonly, but is hard to detect. Average difficulty to exploit. Impact is severe. For prevention, ensure secure app signing, coding practices, testing, and use of trusted third-party libraries or components. Example scenario is malware injection.

---

## References
[Owasp](https://owasp.org/www-project-mobile-top-10/2023-risks/m2-inadequate-supply-chain-security.html)
