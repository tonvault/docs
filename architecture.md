---
description: >-
  Ton Vault Architecture Overview
---

# Architecture Overview

![Architecture](ton-vault.png)

> From a bird's eye view project represents a distributed database of secrets, based on the peer-to-peer (P2P) interaction of nodes. Any participant, if they wish, can launch their own Ton Vault Node and store secrets within it.
> If users launch their own node, they can synchronize their data with a public server, provided by the Ton Vault team (a paid feature) or with any other Ton Vault Node.
> Each client has the right to customize the interface (whether web or application) to interact with their personal storage. By default, however, the application will be synchronized with the Public API.
> The encryption/decryption layer is entirely built upon the user's selected TON Wallet.
> Utilizing the [TON Storage Protocol](https://github.com/.ton-community/ton-docs/tree/main/docs/participate/ton-storage) and an additional encryption layer, users can exchange data amongst each other, thereby creating a decentralized cloud.

## Centralized Part
> The centralized part of the project is represented by the 
> - **Ton Vault Node**
> - **Document-oriented consistent storage ([MongoDB](https://www.mongodb.com/) for instance)** 
> - **Public API gateway**
> 
> Using Public API Gateway, Ton Wallet and official Ton Vault App users can get everything they need to interact with their secrets out of the box.

## Decentralized Part (under development)
> The decentralized part of the project is represented by the network of Ton Vault Nodes, which can communicate with each other using the [TON Storage Protocol](https://github.com/.ton-community/ton-docs/tree/main/docs/participate/ton-storage) and an additional encryption layer.
> Each node provides a built-in API, which allows users to connect official Ton Vault App and Wallet to their own Ton Vault Node.

> Check our [roadmap](roadmap.md) for features that are currently in development.