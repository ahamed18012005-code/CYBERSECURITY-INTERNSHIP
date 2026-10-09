# Task 3 - Mitigation Notes

## 1. SQL Injection

SQL Injection can occur when user input is directly incorporated into SQL queries.

### Recommended Mitigations

* Use prepared statements.
* Use parameterized queries.
* Validate user input.
* Avoid directly concatenating untrusted input into SQL queries.
* Apply appropriate database permissions.

Example parameterized query:
SELECT first_name, last_name FROM users WHERE user = ?

## 2. Cross-Site Scripting (XSS)

XSS occurs when untrusted content is included in a page without suitable handling.

### Output Encoding

The PHP demonstration used:
htmlspecialchars($name, ENT_QUOTES, "UTF-8")

### Content Security Policy

Example policy:
Content-Security-Policy: default-src 'self'; script-src 'self'

### Recommended Mitigations

* Encode untrusted output.
* Validate input where appropriate.
* Avoid placing untrusted content directly into HTML or JavaScript.
* Apply a suitable Content Security Policy.

## 3. Cross-Site Request Forgery (CSRF)

CSRF protection helps prevent unauthorized state-changing requests.

### Recommended Mitigations

* Use unpredictable CSRF tokens.
* Validate tokens on state-changing requests.
* Use SameSite cookies where appropriate.
* Require authentication for sensitive operations.
* Avoid state-changing operations through unsafe GET requests.

### Laboratory Observation

The DVWA High security level used a user_token parameter. The previous forged request was no longer able to change the password.

## 4. File Inclusion

File inclusion risks can arise when applications trust user-controlled file paths.

### Recommended Mitigations

* Validate file-related input.
* Use allowlists for permitted files.
* Restrict accessible directories.
* Avoid directly trusting user-controlled paths.
* Apply appropriate application and server configuration.

### Laboratory Observation

The attempt to access /etc/passwd was unsuccessful and resulted in an application warning.

## 5. HTTP Security Headers

Important headers studied during the task included:

Content-Security-Policy:
Helps restrict permitted content sources.

Strict-Transport-Security:
Helps enforce HTTPS connections.

X-Content-Type-Options:
Helps prevent MIME-type sniffing.

X-Frame-Options:
Controls whether a page can be displayed in frames.

Referrer-Policy:
Controls how referrer information is shared.

Permissions-Policy:
Controls access to selected browser features.

### Example Header Values

X-Content-Type-Options: nosniff

X-Frame-Options: SAMEORIGIN

Referrer-Policy: strict-origin-when-cross-origin

Content-Security-Policy: default-src 'self'; script-src 'self'

## 6. General Security Practices

* Keep web applications and dependencies updated.
* Use secure authentication and authorization.
* Validate inputs and encode outputs.
* Protect state-changing requests.
* Configure appropriate security headers.
* Review application logs and security settings.
* Conduct authorized security testing.

## Ethical Considerations

The testing documented in this task was performed in the controlled local DVWA environment for educational purposes.

## Conclusion

Prepared statements, output encoding, CSRF tokens, file allowlists, and appropriate security headers help reduce common web application risks.
