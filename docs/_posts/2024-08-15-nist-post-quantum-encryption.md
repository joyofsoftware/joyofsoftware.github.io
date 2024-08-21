---
layout: post
title: NIST Post-Quantum Encryption Standards
author: earl
tags: security
excerpt: Quantum computers are often covered in the news with a doomsday message about how their computing power will render encryption obsolete and break the internet. The cryptographic community has been working diligently toward developing new algorithms and standards to provide encryption even as quantum computing capabilities continue to advance.
---
[Quantum computers](https://en.wikipedia.org/wiki/Quantum_computing){:target="_blank"}{:rel="noopener noreferrer"} are often covered in the news with a [doomsday message](https://www.scientificamerican.com/article/tomorrows-quantum-computers-threaten-todays-secrets-heres-how-to-protect-them-2/){:target="_blank"}{:rel="noopener noreferrer"} about how their computing power will render encryption obsolete and break the internet. The cryptographic community has been working diligently toward developing new algorithms and standards to provide encryption even as quantum computing capabilities continue to advance.

Current public-key encryption algorithms depend on three hard math problems that make discovery of encryption keys sufficiently difficult to prevent unwanted decryption: integer factorization (RSA public-key), discrete logarithm (Diffie-Hellman key exchange and Elgamal encryption), and elliptic curve discrete logarithm (Elliptic Curve Diffie-Hellman, ECDSA and ECIES). Thirty years ago in 1994, mathematician [Peter Shor](https://en.wikipedia.org/wiki/Peter_Shor){:target="_blank"}{:rel="noopener noreferrer"} developed a quantum algorithm that reduced the complexity of these hard problems to polynomial time, potentially unlocking the aforementioned encryption when (if?) a sufficiently capable quantum computer is built.

In [December 2016](https://www.nist.gov/news-events/news/2016/12/nist-asks-public-help-future-proof-electronic-information){:target="_blank"}{:rel="noopener noreferrer"}, the US Department of Commerce’s National Institute of Standards (NIST) launched an effort to develop algorithms to ensure ongoing security. In July of 2022, NIST released the drafts for comments and has now finalized the first three post-quantum [encryption standards](https://www.nist.gov/news-events/news/2024/08/nist-releases-first-3-finalized-post-quantum-encryption-standards){:target="_blank"}{:rel="noopener noreferrer"}:

FIPS 203 - a general encryption standard based on Module-Lattice-Based Key-Encapsulation Mechanism (ML-KEM).

FIPS 204 - a digital signature standard based on Module-Lattice-Based Digital Signature Algorithm (ML-DSA)

FIPS 205 - another digital signature standard based on Stateless Hash-Based Digital Signature Algorithm (SLH-DSA). FIPS 205 while slower than FIPS 204 uses a different mathematical approach and is valuable as a backup standard.

A fourth standard is expected later this year with additional standards providing backup algorithms in development. NIST is strongly encouraging wide adoption of the newly released standards.

Note: while the common public-key cryptographic systems are susceptible to quantum computing attacks, there is no similar quantum speed-up that affects other types of cryptography including the very popular symmetric-key Advanced Encryption Standard (AES).
