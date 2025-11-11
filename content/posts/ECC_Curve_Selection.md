+++
date = '2025-11-10T00:00:00+05:00'
draft = true
title = 'Curve selection for Digital Signatures'
+++

This article explores the most feasible curve for Elliptic Curve Cryptography for the use case of Document Signing as per recommendations from the Guideline/standards formulating bodies.

# National Institute for Standards and Technology (NIST)
As per NIST’s recommendations (see NIST SP 800-186) P-256, P-384, P-521 (for ECDSA) and Curve25519 and Curve448 (for EdDSA) are recommended as shown below: 
<insert first table here.>

# WebTrust & CAB Forum
WebTrust or CA/B forum doesn’t have a dedicated requirements/standard for Document Signing use-case, however, the S/MIME requirements (both in WebTrust and CA/Browser forum) cover this use-case under multi-purpose certificates. Both documents specify the curves used while using Elliptic Curve Cryptography (ECC) as following:
__ECDSA__:
* P-256
* P-384
* P-521

__EdDSA__:
* Curve25519
* Curve448

# European Telecommunications Standards Institute (ETSI)
As per ETSI TS 119 312 V1.4.3 (2023-08) (Technical Specifications for Electronic Signatures and Infrastructures (ESI); Cryptographic Suites) following are the recommended elliptic curves for their usage in electronic signatures:
<insert table here.>

# Computational Complexity
As per NIST’s publication NIST Special Publication 800-57 Part 1 Revision 5, following are the comparable security strengths (i.e. brute force effort it takes to break an algorithm) of symmetric block cipher (i.e. AES) and asymmetric algorithms (i.e. ECDSA, EdDSA, etc.)
<insert table with blue top here.>

As per the above table, P256 has comparable security strength as of AES-128, P-384 with AES-192 and P-521 with AES-256.

# Conclusion:
In view of the above, P-256 (also known as secp256r1 and prime256v1), P-384 and P-521 are hereby recommended for using Elliptic Curve algorithm in the context of document signing. For non-extended validity (read as normal/routine) usage, P-256 may be considered as the preferred option.