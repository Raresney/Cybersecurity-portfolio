# Path Traversal

Path traversal (directory traversal) allows an attacker to read arbitrary files on the server by manipulating file paths in application parameters.

---

## Key Concepts

- Exploiting file path parameters (e.g., `?filename=../../../etc/passwd`)
- Bypassing filters: double encoding (`%252e%252e%252f`), null bytes, nested traversal (`....//`)
- Absolute path bypass: using `/etc/passwd` directly
- Stripping defenses: when app strips `../`, use `....//` so stripping leaves `../`
