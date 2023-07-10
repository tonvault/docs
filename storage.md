---
description: >-
  Storage scheme for user data
---

# Storage

>Ton Vault is powered by [TON Storage](https://github.com/.ton-community/ton-docs/tree/main/docs/participate/ton-storage), allowing anyone to host and share files by their ID's. Ton Vault ensures the encryption of user data both on client side and on node server. The latter  is performed with user-provided key, preventing data leaks and allowing serverless decryption.

>Decentralized storage model provides an ability to participate in data storing an sharing to harden against service unavailability. To achieve that, TON Storage [daemon](https://docs.ton.org/participate/ton-storage/storage-daemon) should be used. The latest user's file could be requested from the Ton Vault node using user's public key:

```
axios({
  method: 'get',
  url: 'tonVaultApiUrl',
  data: {
    Authorization: `Bearer ${pubKey}`,
  },
  responseType: {
    result: string,
    code: number
  }
});
```

>To decrypt user data in absence of Ton Vault application, one should generate 2 encryption keys and use them in order, see more in [Crypto](crypto.md) section.

>The uploaded data can't be modified but can be removed and replaced with a new version in the Ton Vault node and in the app. The authorization for user's data management is performed with the [Ton Connect](https://docs.ton.org/develop/dapps/ton-connect/), specifically [ton_proof](https://github.com/ton-blockchain/ton-connect/blob/main/requests-responses.md#address-proof-signature-ton_proof) method.

> Ton Vault nodes communicate using the [ADNL](https://docs.ton.org/learn/networking/adnl) and [TON Storage](https://github.com/.ton-community/ton-docs/tree/main/docs/participate/ton-storage) protocols, but for user convenience and seamless integration, each node is equipped with an HTTP API.
