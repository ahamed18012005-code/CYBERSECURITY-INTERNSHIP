# Task 3 - Attack Scenarios

## 1. SQL Injection

### Objective

To understand how unsafe input handling can allow SQL queries to be manipulated.

### Tests Performed

Normal input:
1

SQL Injection test:
1' OR '1'='1' #

UNION-based test:
1' UNION SELECT user,password FROM users #

### Result

SQL Injection was successfully demonstrated in the controlled DVWA environment. The UNION-based test returned laboratory usernames and password hashes.

## 2. Stored Cross-Site Scripting (XSS)

### Objective

To examine the execution risk associated with untrusted content stored by a web application.

### Test Payload

<img src=x onerror=alert('Stored XSS')>

### Result

Stored XSS was successfully demonstrated in DVWA.

## 3. Reflected Cross-Site Scripting (XSS)

### Objective

To examine the risk of user input being reflected into a web page without suitable output encoding.

### Test Payload

<script>alert('Reflected XSS')</script>

### Result

Reflected XSS was successfully demonstrated in DVWA.

## 4. Cross-Site Request Forgery (CSRF)

### Objective

To compare CSRF behavior at different DVWA security levels.

### Low Security

A forged password-change request successfully demonstrated the vulnerability.

### High Security

A user_token parameter was observed. The previous forged request was no longer able to change the password.

### Result

CSRF was demonstrated at Low security, and token-based protection was observed at High security.

## 5. File Inclusion

### Objective

To examine file inclusion behavior and test whether a local system file could be disclosed.

### Test

../../../../etc/passwd

### Result

The Local File Inclusion attempt was unsuccessful and resulted in an application warning. Successful system-file disclosure was not achieved.

## 6. Burp Suite

### Configuration

Proxy Address: 127.0.0.1
Proxy Port: 8080

### Result

The proxy listener was running, but reliable DVWA traffic interception could not be completed. No successful request modification or Intruder fuzzing result is claimed.

## 7. HTTP Security Headers

### Test

SecurityHeaders.com was used to analyze a safe public test website.

### Result

The website received an F grade from the scanner.

The following headers were studied:

* Content-Security-Policy
* Strict-Transport-Security
* X-Content-Type-Options
* X-Frame-Options
* Referrer-Policy
* Permissions-Policy

## Ethical Consideration

All web security testing was performed in the controlled local DVWA environment. These techniques should only be used on systems for which explicit authorization has been obtained.
