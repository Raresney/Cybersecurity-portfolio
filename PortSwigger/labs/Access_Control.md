# Access Control

Access controls are designed to prevent users from interacting with data or functionality for which they don't have the relevant permissions. Broken access controls are critical bugs that often provide access to more attack surface.

---

## Labs Completed (12/12)

| # | Lab | Level |
| --- | --- | --- |
| 1 | Unprotected admin functionality | Apprentice |
| 2 | Unprotected admin functionality with unpredictable URL | Apprentice |
| 3 | User role controlled by request parameter | Apprentice |
| 4 | User ID controlled by request parameter, with unpredictable user IDs | Apprentice |
| 5 | User ID controlled by request parameter with password disclosure | Apprentice |

---

## Key Concepts

### Vertical Privilege Escalation
- Accessing functions restricted to higher-privilege users
- Unprotected admin pages (direct URL, robots.txt, JS source)
- Unpredictable URLs — still discoverable via page source or JS files

### Horizontal Privilege Escalation
- Accessing another user's resources at the same privilege level
- Manipulating user ID parameters (GUIDs leaked in other responses)

### Horizontal to Vertical Privilege Escalation
- Pivoting from one user's account to an admin account
- Example: accessing admin password via profile page parameter manipulation

### Parameter-Based Access Control
- Role controlled by cookies, hidden fields, or query parameters
- Modifying `admin=true`, `role=admin`, or similar parameters in requests
