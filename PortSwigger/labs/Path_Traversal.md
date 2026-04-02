# Path Traversal

Path traversal (directory traversal) allows an attacker to read arbitrary files on the server by manipulating file paths in application parameters.

---

## Labs Completed (3/3)

| # | Lab | Level |
| --- | --- | --- |
| 1 | File path traversal, simple case | Apprentice |

---

## Key Concepts

### What is Path Traversal?
- Allows reading arbitrary files on the server by manipulating file path parameters
- Can also write to files, potentially modifying application behavior or taking full control

### Reading Arbitrary Files
- Exploiting file path parameters (e.g., `?filename=../../../etc/passwd`)
- Bypassing filters: double encoding (`%252e%252e%252f`), null bytes, nested traversal (`....//`)
- Absolute path bypass: using `/etc/passwd` directly
- Stripping defenses: when app strips `../`, use `....//` so stripping leaves `../`
