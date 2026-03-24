# Public Key Cryptography Basics

## Analogy

| Analogy | Cryptographic System |
|---------|---------------------|
| Secret Code | Symmetric Encryption Cipher and Key |
| Lock | Public Key |
| Lock's Key | Private Key |

## RSA

**RSA** is a public-key encryption algorithm that enables secure data transmission over insecure channels. With an insecure channel, we expect adversaries to eavesdrop on it.

### The Math That Makes RSA Secure

RSA is based on the mathematically difficult problem of **factoring a large number**. Multiplying two large prime numbers is a straightforward operation; however, finding the factors of a huge number takes much more computing power.

It's simple to multiply two prime numbers together even on paper:

```
113 x 127 = 14,351
```

Even for larger prime numbers, it would still be feasible:

```
982,451,653,031 x 169,743,212,279 = 166,764,499,494,295,486,767,649
```

### RSA Variables

| Variable | Description |
|----------|-------------|
| **p** and **q** | Large prime numbers |
| **n** | The product of p and q |
| **Public Key** | n and e |
| **Private Key** | n and d |
| **m** | The original message (plaintext) |
| **c** | The encrypted text (ciphertext) |

## Diffie-Hellman Key Exchange

A method for securely exchanging cryptographic keys over a public channel.

## Digital Signature Algorithms

- **DSA** (Digital Signature Algorithm) -- a public-key cryptography algorithm specifically designed for digital signatures
- **ECDSA** (Elliptic Curve Digital Signature Algorithm) -- a variant of DSA that uses elliptic curve cryptography to provide smaller key sizes for equivalent security
- **ECDSA-SK** (ECDSA with Security Key) -- an extension of ECDSA that incorporates hardware-based security keys for enhanced private key protection
- **Ed25519** -- a public-key signature system using EdDSA (Edwards-curve Digital Signature Algorithm) with Curve25519
- **Ed25519-SK** (Ed25519 with Security Key) -- a variant of Ed25519 that uses a hardware-based security key for improved private key protection

## SSH Key Generation

```bash
ssh-keygen -t ed25519
```

```
Generating public/private ed25519 key pair
```

## GPG (GNU Privacy Guard)

**GPG** stands for GNU Privacy Guard. It is a free and open-source encryption software that uses public-key cryptography. GPG can be used to:

- Encrypt files and messages
- Sign files and messages

---

_Part of [Cybersecurity Portfolio](https://github.com/Raresney/Cybersecurity-portfolio) by Rares Bighiu_
