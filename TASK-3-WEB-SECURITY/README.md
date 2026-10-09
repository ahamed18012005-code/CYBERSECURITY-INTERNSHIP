# Task 3 - Web Application Security

## Overview

Task 3 focused on identifying common web application vulnerabilities and understanding their mitigation techniques using DVWA in a controlled local laboratory environment.

## Lab Environment

* Operating System: Kali Linux
* Web Application: Damn Vulnerable Web Application (DVWA)
* Container Platform: Docker
* DVWA Address: http://127.0.0.1:4280
* Proxy Tool: Burp Suite
* Browser: Firefox
* Security Header Scanner: SecurityHeaders.com
* DVWA Security Levels: Low and High, depending on the test

## Objectives

* Understand SQL Injection.
* Demonstrate Stored and Reflected Cross-Site Scripting (XSS).
* Examine Cross-Site Request Forgery (CSRF).
* Test file inclusion functionality.
* Explore Burp Suite as a web security proxy.
* Review HTTP security headers.
* Understand suitable mitigation techniques.

## Activities Performed

### 1. SQL Injection

SQL Injection was tested using the DVWA SQL Injection module.

The tests demonstrated that unsafe input handling could allow SQL conditions to be manipulated and laboratory database records to be returned.

A UNION-based test also demonstrated retrieval of laboratory usernames and password hashes.

Mitigation:

* Use prepared statements.
* Use parameterized queries.
* Validate user input.
* Safely encode output.

### 2. Stored Cross-Site Scripting (XSS)

Stored XSS was tested using the DVWA Stored XSS module.

The test demonstrated how submitted content could be stored and executed when the affected page was viewed.

### 3. Reflected Cross-Site Scripting (XSS)

Reflected XSS was tested using the DVWA Reflected XSS module.

The test demonstrated the risk of reflecting user-controlled input into a page without appropriate output encoding.

Mitigation:

* Encode untrusted output.
* Validate input.
* Apply an appropriate Content Security Policy.

### 4. Cross-Site Request Forgery (CSRF)

CSRF was tested using the DVWA CSRF module.

At Low security, a forged password-change request successfully demonstrated the vulnerability.

At High security, a CSRF token was observed, and the previous forged request was no longer able to change the password.

### 5. File Inclusion

The DVWA File Inclusion module was examined.

A Local File Inclusion attempt targeting /etc/passwd was unsuccessful and resulted in an application warning.

Successful system-file disclosure was not achieved.

### 6. Burp Suite

Burp Suite was explored as a web application security testing proxy.

* Proxy Address: 127.0.0.1
* Proxy Port: 8080

The proxy listener was running, but reliable interception of DVWA traffic could not be completed.

No successful request modification or Intruder fuzzing result is claimed.

### 7. HTTP Security Headers

SecurityHeaders.com was used to analyze a safe public test website.

The website received an F grade from the scanner.

Headers studied included:

* Content-Security-Policy
* Strict-Transport-Security
* X-Content-Type-Options
* X-Frame-Options
* Referrer-Policy
* Permissions-Policy

## Key Findings

* SQL Injection was successfully demonstrated in DVWA.
* Stored and Reflected XSS were successfully demonstrated.
* CSRF was demonstrated at Low security.
* CSRF token protection was observed at High security.
* The Local File Inclusion attempt was unsuccessful.
* Burp Suite interception remained incomplete.
* HTTP security headers were studied using SecurityHeaders.com.

## Security Recommendations

* Use parameterized SQL queries.
* Encode untrusted output.
* Implement an appropriate Content Security Policy.
* Use CSRF tokens on state-changing requests.
* Restrict file inclusion using allowlists and path validation.
* Configure appropriate HTTP security headers.
* Perform security testing only with authorization.

## Ethical Considerations

Testing was performed against the intentionally vulnerable DVWA application running locally in a controlled laboratory environment.

No unauthorized testing was performed against external systems.

## Conclusion

Task 3 provided practical experience in identifying common web application vulnerabilities and reviewing their mitigation techniques.

The work emphasized secure input handling, output encoding, CSRF protection, file access restrictions, and HTTP security headers.

## Deliverables

* TASK-3-REPORT.pdf
* Attack-Scenarios.md
* Mitigation-Notes.md
