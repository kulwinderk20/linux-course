OWASP: OWASP 10 2021
## Security Misconfiguration
•	A05:2021-Security Misconfiguration: A05:2021-Security Misconfiguration moves up from #6 in the previous edition; 90% of applications were tested for some form of misconfiguration. With more shifts into highly configurable software, it’s not surprising to see this category move up. The former category for XML External Entities (XXE) is now part of this category.
Mismanaged security configurations of web server stack, underlying Operation System, databases, external services. 
- Permissions
- Secret management
- Exposing Error messages 
- Not using [HTTP security headers](https://owasp.org/www-project-secure-headers/), although this not a vulnerability in itself
- No brute force prevention or restrictions on [[Bypassing-Rate-Limits]]
[OWASP top 10 entry for Security Misconfiguration](https://owasp.org/Top10/A05_2021-Security_Misconfiguration/).
 
•	A06:2021-Vulnerable and Outdated Components: A06:2021-Vulnerable and Outdated Components was previously titled Using Components with Known Vulnerabilities and is #2 in the Top 10 community survey, but also had enough data to make the Top 10 via data analysis. This category moves up from #9 in 2017 and is a known issue that we struggle to test and assess risk. It is the only category not to have any Common Vulnerability and Exposures (CVEs) mapped to the included CWEs, so a default exploit and impact weights of 5.0 are factored into their scores.

•	A03:2021-Injection: SQL Injection, 
*Insecure deserialization https://portswigger.net/web-security/deserialization
*Directory traversal https://portswigger.net/web-security/file-path-traversal
*Access control https://portswigger.net/web-security/access-control
*Authentication https://portswigger.net/web-security/authentication
*Auth authentication https://portswigger.net/web-security/oauth
*Business logic vulnerabilities https://portswigger.net/web-security/logic-flaws

Goat. Install webgoat. – I have tried to install in the mac but unable to install, every time getting an error. 
d) Sequel. Solve SQLZoo:
Johnny tables. Solve Portswigger Labs: Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
