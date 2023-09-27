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
- Insecure deserialization https://portswigger.net/web-security/deserialization
- Directory traversal https://portswigger.net/web-security/file-path-traversal
- Access control https://portswigger.net/web-security/access-control
- Authentication https://portswigger.net/web-security/authentication
- Auth authentication https://portswigger.net/web-security/oauth
- Business logic vulnerabilities https://portswigger.net/web-security/logic-flaws

Goat. Install webgoat. – I have tried to install in the mac but unable to install, every time getting an error. 
d) Sequel. Solve SQLZoo:
//http://sqlzoo.net/wiki/Nobel_Quiz
//Table nobel: yr, subject, winner

//Pick the code which shows the name of winner's names beginning with C and ending in n
1. 	SELECT winner FROM nobel 
   		WHERE winner LIKE 'C%' AND winner LIKE 'n%'

//Select the code that shows how many Chemistry awards were given between 1950 and 1960
2. 	SELECT COUNT(subject) FROM nobel
		WHERE yr BETWEEN 1950 AND 1960 
		      AND subject = 'Chemistry'

//Pick the code that shows the amount of years where no Medicine awards were given
3. 	SELECT COUNT(DISTINCT yr) FROM nobel
		WHERE yr NOT IN (SELECT yr FROM nobel 
			WHERE subject = 'Medicine')

4. 	SELECT subject, winner FROM nobel 
		WHERE yr LIKE '196%' and winner LIKE 'Sir%'

//Select the code which would show the year when neither a Physics or Chemistry award was given
5. 	SELECT yr FROM nobel 
		WHERE yr NOT IN 
			(SELECT yr FROM nobel 
				WHERE subject = 'Physics' OR subject = 'Chemistry')
				or
				WHERE subject IN ('Physics', 'Chemistry')

//Select the code which shows the years when a Medicine award was given but no Peace or Literature award was
6. 	SELECT DISTINCT yr FROM nobel 
		WHERE yr NOT IN (
			SELECT yr FROM nobel
				WHERE subject IN ('Peace', 'Literature')
		)
		AND subject = 'Medicine'

7.	SELECT subject, COUNT(subject) FROM nobel
		WHERE yr = '1960' 
		GROUP BY subject
• Johnny tables. Solve Portswigger Labs: Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
