**CSRF (Cross-Site Request Forgery):**

**Definition:** CSRF is an attack where an attacker tricks a user's browser into making an unintended and potentially malicious request on a trusted website where the user is authenticated.

**Prevention in Django:**
- Django protects against CSRF attacks by using a CSRF token mechanism.
- The `CsrfViewMiddleware` adds a hidden input field with a token to each form, and on form submission, the server checks if the token is valid.

**XSS (Cross-Site Scripting):**

**Definition:** XSS is an attack where an attacker injects malicious scripts into web pages that are then executed by the user's browser.

**Prevention in Django:**
- Django provides automatic HTML escaping, which converts special characters to their HTML entities, preventing script execution.
- Developers should use template filters like `safe` cautiously and sanitize user inputs to prevent unintended script execution.

**Clickjacking:**

**Definition:** Clickjacking is an attack where an attacker tricks a user into clicking on something different from what the user perceives, potentially leading to unintended actions.

**Prevention in Django:**
- Django prevents clickjacking by using the `X-Frame-Options` header.
- The `XFrameOptionsMiddleware` sets this header to either deny (prevents framing) or same-origin (allows framing by the same origin).

**Summary:**

- **CSRF:** Protects against unauthorized requests by using tokens in forms to ensure that requests originate from the same site.
- **XSS:** Prevents malicious script injection by automatically escaping HTML content and encouraging developers to sanitize user inputs.
- **Clickjacking:** Guards against clickjacking by setting the `X-Frame-Options` header to prevent unauthorized framing of the web page.

In summary, these security measures in Django help protect web applications from common vulnerabilities such as unauthorized requests, script injection, and clickjacking, contributing to a more secure web environment.
