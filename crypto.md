---
description: >-
  Ton Vault's cryptography protocol overview
---

# Crypto
>Since Ton Vault is accessible via TON Storage, all user sensitive data must be encrypted. AES-256-CBC mode is used for client-side local encryption with key generated from SHA256-hashed user-signed message. 

>To ensure only encrypted data in storage, the process is duplicated on the server side. User generates a key for server-side encryption by hashing previous obtained key again.

>Message to be signed with user's private key contains SHA256 of data to be encrypted:
``--TON VAULT KEY GENERATION MESSAGE--\n${rawContentHash}``
If the user's wallet doesn't support signing UTF-8 strings, this message would be displayed as human-unreadable HEX string.
**Warning** Signature compromise would result in signer's stored data leak.

>The `rawContentHash` hash is stored alongside encrypted data in the same Bag of Cells (BoC) to maintain ability to decrypt file without Ton Vault app. 
