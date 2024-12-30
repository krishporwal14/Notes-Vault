<center><h1>M3 - Insecure Authentication, Authorization</h1></center>

## Metadata
- **Date:** 25/12/2024  
- **Tags:** [[cybersecurity]] [[apphacking]] [[year2024]] [[android]] [[mobile]] [[binary attacks]] [[privilege escalation]] [[unauthorized access]] [[Insecure Direct Object Reference (IDOR)]]
- **Author/Name:** Krish Porwal

---

## Theory
#### Threat Agents
- Application Specific.
- Typically through automated attacks.

#### Attack Methods
- <u>Easy</u> to exploit.
- Two ways to exploit-
	1. Bypass the authentication by directly interacting with the backend server instead of the mobile app.
	2. Logging in as a legitimate user.
- Accomplished using mobile malware or botnets.

#### Security Weakness
- Occurrence is <u>common</u>.
- Detectability is <u>average</u>.
- For authorization,
	1. Testers can perform [[binary attacks]].
	2. Try to perform privileged functionalities especially when the mobile app is in 'offline mode'.
	3. Also test low-privilege session tokens within the respective POST/GET requests for sensitive functionality to the backend server.
	4. Leads to [[privilege escalation]] attack.
	5. Risk is heightened when authorization decisions are made within the mobile app (to provide offline usability) instead of a remote server.
- For authentication,
	1. Testers can perform [[binary attacks]] when the mobile app is 'offline'.
	2. Also try to execute any backend server functionality anonymously by removing any session tokens from any POST/GET requests.
	3. Poor authentication can allow an adversary to anonymously execute functionality within the mobile app or the backend server.
	4. These weaknesses are common due to the mobile device's input form factor, which often encourages short passwords or 4-digit PINs.
	5. ![[Pasted image 20241225110433.png]]

#### Impacts
- Both Technical and Business impacts are <u>severe</u>.
- Technical impacts include failure to identify the user performing an action request, leading to inability to log or audit user activity. This lack of identity verification leads to the inability to detect the source of the attack, understand any underlying exploits, or devise strategies to prevent future attacks. Failures in authentication can expose underlying authorization failures. Inability to determine user's identity which is tied to user roles and permissions leads to [[unauthorized access]]. **Anonymous execution of code leads to failures in both authentication and authorization controls**.
- Business impacts include reputation damage, information theft, fraud, [[unauthorized access]] to the data.

#### Who is vulnerable?
- Authentication identifies an individual, while authorization verifies if the identified individual has the necessary permissions for a particular action.
- An authorization check should be performed after authentication.
- Insecure authorization-
	1. Presence of [[Insecure Direct Object Reference (IDOR)]] vulnerabilities.
	2. Hidden endpoints.
	3. User role or permission transmission.
- Insecure authentication-
	1. Anonymous Backend API Execution.
	2. Local Storage of passwords or shared secrets (Like in [[M1 - Improper Credential Usage]]).
	3. Weak password policy.
	4. Usage of features like FaceID and TouchID.

#### Prevention
- Avoid weak patterns.
- Perform all authentication requests server-side.
- Encrypt data stored at client side.
- The 'Remember Me' functionality should never store user passwords on the client side.
- Avoid using spoof-able values for user authentication.
- Use a device-specific device authentication token.
- Refrain from using 4-digit pins.
- Persistent authentication should be optional.
- Reinforcing server-side authentication and authorization controls.
- Backend system should independently identify roles and permissions of authenticated users.
- Perform local integrity checks to detect unauthorized code changes.

---

## Scenarios
![[Pasted image 20241225114941.png]]

![[Pasted image 20241225114956.png]]

---

## Summary
> Occurs due to insecure authentication and authorization when performed offline i.e. client-side or absence of authorization tokens. Occurs commonly and detectability is average. Impact is severe.

---

## References
[Owasp](https://owasp.org/www-project-mobile-top-10/2023-risks/m3-insecure-authentication-authorization.html)
