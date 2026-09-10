# Practical 4: Cryptography for Data Privacy

## Aim

To understand the role of cryptography in protecting personal and sensitive data and to study different cryptographic techniques used for data privacy.

## Introduction

Cryptography is the technique of protecting information by converting it into a form that unauthorized users cannot easily understand. It helps provide confidentiality, integrity, authentication and data protection.

## Major Cryptographic Techniques

### 1. Symmetric Encryption

Symmetric encryption uses the **same secret key** for both encryption and decryption.

```text
Plaintext
    ↓
Encryption + Secret Key
    ↓
Ciphertext
    ↓
Decryption + Same Key
    ↓
Plaintext

Example: AES

Applications:

Database encryption
File encryption
Secure storage
Protection of sensitive information
2. Asymmetric Encryption

Asymmetric cryptography uses a pair of mathematically related keys:

Public Key – can be shared with others.
Private Key – must be kept secret.
Public Key
    ↓
Encryption
    ↓
Ciphertext
    ↓
Private Key
    ↓
Decryption
    ↓
Original Data
Examples: RSA and ECC

Applications:

Secure communication
Key exchange
Digital signatures
Authentication
3. Hashing

Hashing converts input data into a fixed-length value called a hash.

Input Data
    ↓
Hash Function
    ↓
Hash Value

Examples: SHA-256, SHA-3

Applications:

Data integrity verification
Password protection
File verification

4. Digital Signatures

A digital signature uses asymmetric cryptography to verify the authenticity and integrity of digital information.

Message
    ↓
Hash Function
    ↓
Message Hash
    ↓
Private Key
    ↓
Digital Signature

The receiver can use the sender's public key to verify the signature.
Applications:

Digital documents
Software signing
Digital certificates
Authentication

Cryptography and Data Privacy
Cryptographic techniques protect data at different stages of its lifecycle:

| Data State / Purpose | Cryptographic Technique | Example                     |
| -------------------- | ----------------------- | --------------------------- |
| Data in Transit      | Encryption              | HTTPS/TLS                   |
| Data at Rest         | Encryption              | Encrypted database          |
| Password Protection  | Password Hashing        | Argon2, bcrypt              |
| Data Integrity       | Hashing                 | File integrity verification |
| Authentication       | Digital Signatures      | Digital certificates        |

Example: Online Educational Platform

For an online educational platform, cryptographic techniques can help protect:

User account information
Login credentials
Communication between users and servers
Sensitive stored information
Data transmitted over the internet

HTTPS/TLS helps protect information while it is being transmitted between a user's browser and the server.

Privacy Risks Without Cryptography

Without appropriate cryptographic protection:

Attackers may intercept sensitive information.
Stored information may be exposed after unauthorized access.
Data may be modified without detection.
User credentials may be compromised.
Communication may become vulnerable to interception.
Recommended Security Practices
Use modern and well-tested cryptographic algorithms.
Use HTTPS/TLS to protect data in transit.
Encrypt sensitive data stored on servers.
Never store passwords in plain text.
Use secure password-hashing algorithms.
Protect cryptographic keys using secure key-management practices.
Avoid outdated or weak cryptographic algorithms.

Difference Between Encryption and Hashing

| Feature      | Encryption                    | Hashing                            |
| ------------ | ----------------------------- | ---------------------------------- |
| Main Purpose | Protect confidentiality       | Protect integrity                  |
| Reversible   | Yes, with the appropriate key | Designed to be one-way             |
| Uses a Key   | Usually                       | No secret key for ordinary hashing |
| Example      | AES                           | SHA-256                            |
| Example Use  | Encrypting files              | Integrity checking                 |

Conclusion

Cryptography is an important technology for data privacy and cybersecurity. Symmetric encryption protects data efficiently, asymmetric cryptography supports secure communication and authentication, hashing helps verify data integrity, and digital signatures provide authenticity and integrity.

Using appropriate cryptographic techniques can significantly reduce the risk of data exposure, unauthorized modification and communication attacks
