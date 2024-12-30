<center><h1>M4 - Insufficient Input Output Validation</h1></center>

## Metadata
- **Date:** 30/12/2024  
- **Tags:** [[cybersecurity]] [[apphacking]] [[year2024]] [[android]] [[mobile]] [[SQL Injection]] [[Command Injection]] [[Cross-Site Scripting (XSS)]] [[unauthorized access]] [[Path Traversal]] [[session hijacking]] [[penetration testing]]
- **Author/Name:** Krish Porwal

---

## Theory
#### Threat Agents
- Application Specific
- Insufficient validation and sanitization of data from external sources, such as user inputs or network data, are at risk of being exploited through attacks such as [[SQL Injection]], [[Command Injection]], and [[Cross-Site Scripting (XSS)]] attacks.
- May lead to [[unauthorized access]], manipulation of app functionality, and potential compromise of the entire mobile system.
- Inadequate output validation can result in data corruption or presentation vulnerabilities, allowing actors to inject malicious code or manipulate sensitive information displayed to users.

#### Attack Methods
- <u>Difficult</u> to exploit.
- Exposes the app to [[SQL Injection]], [[Cross-Site Scripting (XSS)]], [[Command Injection]], and [[Path Traversal]].
- Can lead to [[unauthorized access]], data manipulation, code execution, and compromise of the entire backend system.

#### Security Weakness
- Occurrence is <u>common</u>.
- <u>Easy</u> to detect.
- Can be exploited in the following ways-
	1. Insufficient Input Validation.
	2. Insufficient Output Validation ([[Cross-Site Scripting (XSS)]], [[session hijacking]], data theft).
	3. Lack of Contextual Validation.
	4. Failure to Validate Data Integrity.
- Arise from errors in application logic, incomplete implementation of validation checks, or insufficient testing and code review practices.

#### Impacts
- Both Technical and Business impacts are <u>severe</u>.
- Technical impacts are code execution, data breaches, system compromise, application disruption, reputation damage, and legal and compliance issues.

#### Who is vulnerable?
Application with,
- Lack of Input Validation.
- Inadequate Output Sanitization.
- Context-Specific Validation Neglect.
- Insufficient Data Integrity Checks.
- Poor Secure Coding Practices.

#### Prevention
- Use strict user input validation strategies.
- Put input length restrictions and reject unexpected or malicious data.
- Use output encoding techniques.
- Perform specific validation on data context (file uploads).
- Use parameterized queries and prepared statements to prevent [[SQL Injection]].
- Conduct [[penetration testing]] and code reviews.

---

## Scenarios
![[Pasted image 20241230192148.png]]

![[Pasted image 20241230192157.png]]

---

## Summary
> May leave the application vulnerable to [[SQL Injection]], [[Command Injection]], [[Cross-Site Scripting (XSS)]], [[unauthorized access]], etc. Difficult to exploit, common occurrence, and easy to detect. Severe technical and business impacts. Can be prevented using strict user input validation techniques, output encoding, [[penetration testing]], data integrity checks.

---

## References
[Owasp](https://owasp.org/www-project-mobile-top-10/2023-risks/m4-insufficient-input-output-validation.html)
