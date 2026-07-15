# Insecure Direct Object Reference (IDOR)

## Overview

An Insecure Direct Object Reference (IDOR) vulnerability was identified in the basket functionality. The application exposed resources by referencing predictable object identifiers without enforcing proper server-side authorization checks.

**Severity:** High

---

## Affected Component

- Basket Functionality
- GET /rest/basket/{id}

---

## Tools

- Burp Suite Community Edition
- Chromium

---

## Reproduction

1. Configure Burp Suite Community Edition as the browser's intercepting proxy.
2. Enable request interception.
3. Navigate to:

```text
http://localhost:3000/#/basket
```

4. Intercept the HTTP request sent to:

```text
GET /rest/basket/{id}
```

5. Modify the `{id}` path parameter to another valid basket identifier.
6. Forward the modified request to the server.
7. Observe that the application returns another user's basket, confirming an IDOR vulnerability.

---

## Evidence

- Original intercepted request.
- Modified request.
- Server response showing another user's basket.

![IDOR ID 0](../screenshots/idor%200.jpg)
![IDOR ID 1](../screenshots/idor%201.jpg)
![IDOR ID 2](../screenshots/idor%202.jpg)
---

## Impact

In a real-world application, this vulnerability could allow unauthorized users to access or manipulate resources belonging to other users, potentially resulting in sensitive data exposure or unauthorized actions.

---

## Recommendation

- Enforce server-side authorization checks.
- Verify resource ownership before returning data.
- Avoid relying solely on object identifiers for access control.
- Apply the principle of least privilege.

---

## References

- OWASP Top 10 – Broken Access Control
- OWASP Web Security Testing Guide