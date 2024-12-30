<center><h1>M5 - Insecure Communication</h1></center>

## Metadata
- **Date:** 30/12/2024  
- **Tags:** [[cybersecurity]] [[apphacking]] [[year2024]] [[android]] [[mobile]] [[privacy violation]] [[certificate pinning]]
- **Author/Name:** Krish Porwal

---

## Theory
#### Threat Agents
- Application Specific.
- May have different motives such as stealing sensitive information, conducting espionage, identity theft, and more.
- The following are the threat agents-
	1. An adversary that shares your local network (compromised or monitored Wi-Fi).
	2. Rogue carrier or network devices (routers, cell towers, proxy's, etc).
	3. Malware on your mobile.

#### Attack Methods
- <u>Easy</u> to exploit.
- Even though modern applications use cryptographic protocols such as SSL/TLS, they can also have flaws in their implementation such as,
	- Using deprecated protocols and/or bad configuration settings.
	- Accepting bad SSL certificates (such as self-signed, revoked, expired, wrong host).
	- Inconsistency (having SSL/TLS only on specific workflows).

#### Security Weakness
- <u>Common</u> occurrence.
- <u>Average</u> to detect.

#### Impacts
- Technical impacts are <u>severe</u> and business impacts are <u>moderate</u>.
- Can expose user data, which might lead to account takeover, user impersonation, PII Data Leaks and more.
- Business impacts include [[privacy violation]] which may result in identity theft, fraud, or reputational damage.

#### Who is vulnerable?
- Usual risks of insecure communication are around data integrity, data confidentiality, and origin integrity.
- For example, data being changed in transit without being detected, or leakage of confidential data by observation of communication, or failure of properly setting up and validating a TLS connection.

#### Prevention
Best practices include,
- Apply SSL/TLS to transport channels.
- Avoid mixed SSL sessions as they might expose user's session ID.
- Use strong, industry standard cipher suites with appropriate key lengths.
- Use certificates signed by a trusted CA provider.
- Never allow bad certificates.
- Consider [[certificate pinning]].
- Always require SSL chain verification.
- Do not send sensitive data over alternate channels such as SMS.
- Provide an extra layer of encryption to data.

---

## Scenarios
![[Pasted image 20241230213721.png]]

![[Pasted image 20241230213735.png]]

---

## Summary
> The attackers can exploit vulnerabilities in the insecure communication channels and steal important information, identity, etc. Easy to exploit, occurrence is common, average to detect. Technical impact is severe and business impact is moderate. Using deprecated SSL/TLS versions or bad configuration settings may lead to this. Use well configured SSL/TLS channels on all workflows, provide another layer of data encryption, and check certificates more strictly and accept only those from a trusted CA provider.

---

## References
[Owasp](https://owasp.org/www-project-mobile-top-10/2023-risks/m5-insecure-communication.html)
