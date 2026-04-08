# File Upload Vulnerabilities

Any functionality that enables users to upload files to the server's filesystem is inherently dangerous. Failing to enforce proper restrictions on uploaded files can enable an attacker to run arbitrary system commands, giving them full control over the server.

---

## Labs Completed (9/9)

| # | Lab | Level |
| --- | --- | --- |
| 1 | Remote code execution via web shell upload | Apprentice |
| 2 | Web shell upload via Content-Type restriction bypass | Apprentice |
| 3 | Web shell upload via path traversal | Practitioner |
| 4 | Web shell upload via extension blacklist bypass | Practitioner |
| 5 | Web shell upload via obfuscated file extension | Practitioner |
| 6 | Remote code execution via polyglot web shell upload | Practitioner |
| 7 | Web shell upload via race condition | Expert |
| 8 | URL-based file upload | Practitioner |
| 9 | File upload with no Content-Type validation | Apprentice |

---

## Key Concepts

### Web Shell Upload
- Uploading executable scripts (e.g., `.php`, `.jsp`) to gain RCE
- Simple case: no validation on file type or extension

### Bypassing Upload Defenses
- Content-Type manipulation: changing MIME type to `image/jpeg` while uploading `.php`
- Extension bypass: using alternative extensions (`.php5`, `.phtml`, `.shtml`)
- Obfuscated extensions: null bytes (`file.php%00.jpg`), double extensions, case variation
- Path traversal: uploading to a directory where execution is allowed
- Polyglot files: embedding malicious code inside valid image files

### Race Conditions
- Exploiting the window between file upload and server-side validation/cleanup
- Sending rapid requests to execute the file before it is deleted
