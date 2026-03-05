CertiCrypt

CertiCrypt is an enhanced fork of the open-source project CryptoPocket created by Miroslav Pejić. The original project provides functionality for encrypting text, files, and credentials using symmetric cryptography.

CertiCrypt extends CryptoPocket by introducing Public Key Infrastructure (PKI) based security features such as digital signatures, certificate-based authentication, hybrid encryption, and secure key management. These improvements transform the original application into a more complete cryptographic security tool capable of addressing real-world security challenges.

Original Project:
https://github.com/miroslavpejic85/cryptopocket

Overview

CertiCrypt is a portable cryptographic utility that allows users to securely:

Store encrypted credentials

Encrypt and decrypt files

Encrypt and decrypt text messages

Generate secure passwords

Digitally sign documents

Verify digital signatures

Securely exchange encrypted files using PKI mechanisms

The application is implemented using VB.NET (.NET Framework 4.8) and builds upon the architecture of the original CryptoPocket project.

No installation is required. The application can run as a portable desktop tool.

Key Security Features

CertiCrypt integrates modern cryptographic mechanisms designed to ensure:

Confidentiality

Integrity

Authentication

Encryption and Confidentiality

CertiCrypt uses AES-256 symmetric encryption to encrypt files and text messages.

Encryption keys are derived using PBKDF2 (Rfc2898DeriveBytes) to ensure strong password-based key generation.

Encrypted files and messages can only be decrypted using the correct key.

Digital Signatures

CertiCrypt introduces digital signature functionality that allows users to sign files and verify their authenticity.

Digital signatures provide:

Authentication — verifying the identity of the signer

Integrity — ensuring documents have not been modified

Non-repudiation — preventing signers from denying authorship

This feature is particularly useful for secure document distribution and verification.

Certificate-Based Authentication

CertiCrypt leverages Public Key Infrastructure (PKI) to authenticate users using digital certificates.

Certificates bind a user’s identity to their public key and enable secure communication between trusted parties.

The system supports:

Public/private key generation

Certificate validation

Secure identity verification

Hybrid Encryption

CertiCrypt implements hybrid encryption, combining symmetric and asymmetric cryptography.

Workflow

A random AES key encrypts the file or message.

The AES key is encrypted using the recipient’s public key.

The recipient decrypts the AES key using their private key.

This approach ensures both:

High performance

Secure key exchange

Secure Key Management

Private keys are stored securely using password-protected keystores, helping prevent unauthorized access and protecting sensitive cryptographic material.

The system also supports certificate revocation mechanisms to invalidate compromised keys.

Core Features

CertiCrypt provides several integrated features designed to improve security and usability.

Secure Credential Storage

CertiCrypt allows users to create a local encrypted credential database where login details can be stored securely.

Stored fields include:

Description

Email address

Website URL

Username

Password

Credentials are encrypted before being stored and can only be viewed when the correct encryption key is provided.

Text Encryption and Decryption

Users can encrypt and decrypt text messages directly within the application.

Text can be:

Written manually

Imported from a TXT file

The encrypted output can be saved and later decrypted using the appropriate key.

File Encryption

CertiCrypt supports encryption and decryption of files of any format.

Encrypted files are stored locally and can only be decrypted using the correct key.

Random Password Generation

The system includes a secure password generator that uses cryptographically secure random number generation.

Users can generate passwords with customizable parameters such as:

Length

Character types

Special characters

This feature helps users create strong credentials for online accounts.

Improvements Over CryptoPocket

While CryptoPocket provides basic encryption functionality, it lacks several security features required in modern cryptographic systems.

CertiCrypt addresses these limitations.

Feature	CryptoPocket	CertiCrypt
AES File Encryption	Yes	Yes
Password Generation	Yes	Yes
Credential Storage	Yes	Yes
Digital Signatures	No	Yes
Certificate Authentication	No	Yes
Hybrid Encryption	No	Yes
Secure Key Management	Limited	Improved
PKI Integration	No	Yes

These enhancements significantly improve the system’s ability to secure communications and verify user identity.

Example Use Cases

CertiCrypt can be applied to several real-world scenarios.

Secure Document Signing

Users can digitally sign documents and verify signatures to ensure authenticity and prevent tampering.

Secure File Sharing

Files can be encrypted and securely transmitted between users using hybrid encryption.

Credential Management

Users can securely store login credentials in an encrypted local database.

Installation and Usage
Requirements

Windows OS

.NET Framework 4.8

Visual Studio (for building from source)

Running the Application
Clone the repository
git clone https://github.com/yourusername/certicrypt.git
Open the solution in Visual Studio
CryptoPocket.sln
Build the project

Compile the solution using Visual Studio.

Run the application

Run the generated executable from the build directory.

Project Structure
src/
│
├── Class/
│   ├── Cryptology.vb
│   ├── RandomKeyGenerator.vb
│   └── RandomP.vb
│
├── Forms/
│   └── Main.vb
│
├── Resources/
│   └── UI assets and icons
│
├── CryptoPocket.sln
└── CryptoPocket.vbproj

Contributing

Contributions are welcome and encouraged.

Developers can help improve CertiCrypt by:

Adding additional cryptographic features

Improving security mechanisms

Refactoring the codebase

Implementing automated testing

Pull requests and suggestions are greatly appreciated.

Attribution

CertiCrypt is based on the open-source project CryptoPocket developed by Miroslav Pejić.

Original repository:
https://github.com/miroslavpejic85/cryptopocket

The project is distributed under the MIT License, which permits modification and redistribution.

License

MIT License

Copyright (c) 2021 Miroslav Pejić

Modified and extended as CertiCrypt for academic research and development.
