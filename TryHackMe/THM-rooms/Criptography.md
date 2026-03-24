# Cryptography

Cryptography is used to protect **confidentiality**, **integrity**, and **authenticity**. In this age, you use cryptography daily, and you're almost certainly reading this over an encrypted connection.

Cryptography's history is long and dates back to ancient Egypt in **1900 BCE**. However, one of the simplest historical ciphers is the **Caesar Cipher** from the first century BCE. The idea is simple: shift each letter by a certain number to encrypt the message.

### Historical Ciphers

- The **Vigenere cipher** from the 16th century
- The **Enigma machine** from World War II
- The **one-time pad** from the Cold War

### Relevant Standard

- **Payment Card Industry Digital Security Standard (PCI DSS)**

## Key Terminology

| Term | Definition |
|------|------------|
| **Plaintext** | The original, readable message or data before it's encrypted. It can be a document, an image, a multimedia file, or any other binary data. |
| **Ciphertext** | The scrambled, unreadable version of the message after encryption. Ideally, we cannot get any information about the original plaintext except its approximate size. |
| **Cipher** | An algorithm or method to convert plaintext into ciphertext and back again. A cipher is usually developed by a mathematician. |
| **Key** | A string of bits the cipher uses to encrypt or decrypt data. The used cipher is generally public knowledge; however, the key must remain secret unless it is the public key in asymmetric encryption. |
| **Encryption** | The process of converting plaintext into ciphertext using a cipher and a key. Unlike the key, the choice of the cipher is disclosed. |
| **Decryption** | The reverse process of encryption, converting ciphertext back into plaintext using a cipher and a key. Recovering the plaintext without knowledge of the key should be impossible (infeasible). |

## XOR

If this is the first time you work with a truth table, it is a table that shows all possible outcomes. The XOR truth table states all four cases:

| A | B | A XOR B |
|---|---|---------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
