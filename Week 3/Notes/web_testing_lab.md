# Web Application Testing Lab

## Objective
To identify and exploit vulnerabilities in a web application (DVWA) using both manual and automated techniques.

---

## Tools Used
- DVWA
- SQLMap
- Browser Developer Tools

---

## Vulnerabilities Tested

### 1. SQL Injection
Manual testing was performed using input payloads such as `' OR 1=1 --`. The application returned database results, confirming vulnerability.

SQLMap was used to automate the attack and extract databases, tables, and user credentials.

---

### 2. Cross-Site Scripting (XSS)

#### Reflected XSS
A script payload was injected into input fields and executed immediately.

#### Stored XSS
A payload was stored in the database and executed whenever the page was loaded.

---

## Result
Multiple vulnerabilities were identified, including SQL Injection and XSS. Sensitive data such as usernames and passwords were extracted.

---

## Conclusion
The application is highly vulnerable and lacks proper input validation and output encoding mechanisms.
