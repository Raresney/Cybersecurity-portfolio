# Authentication

Authentication is the process of checking that a user really is who they claim to be. Flawed authentication mechanisms may allow an attacker to guess valid sets of credentials by automating thousands of login attempts using specialist tools like Burp Intruder.

---

## Labs Completed (10/10)

| # | Lab | Level |
| --- | --- | --- |
| 1 | Username enumeration via different responses | Apprentice |
| 2 | Username enumeration via subtly different responses | Practitioner |
| 3 | Username enumeration via response timing | Practitioner |
| 4 | Broken brute-force protection, IP block | Practitioner |
| 5 | Username enumeration via account lock | Practitioner |
| 6 | 2FA simple bypass | Apprentice |
| 7 | 2FA broken logic | Practitioner |
| 8 | Brute-forcing a stay-logged-in cookie | Practitioner |
| 9 | Offline password cracking | Practitioner |
| 10 | Password reset broken logic | Apprentice |

---

## Key Concepts

### Brute-Force Attacks
- Automated credential guessing using wordlists
- Username enumeration via differing responses, timing, or account lockouts
- Bypassing IP-based brute-force protection by alternating valid/invalid logins

### Multi-Factor Authentication (2FA)
- Simple bypass: navigating directly past the 2FA check after login
- Broken logic: manipulating verification parameters to target other accounts
- Brute-forcing 2FA codes when no rate limiting is enforced

### Stay-Logged-In Cookies
- Predictable cookie construction (e.g., base64-encoded `username:md5(password)`)
- Offline cracking via XSS-stolen cookies

### Password Reset Flaws
- Token-based reset flows with missing or weak validation
- Manipulating parameters to reset another user's password
