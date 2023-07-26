---
description: >-
  Ton Vault Architecture Overview
---

# Architecture Overview

![Architecture](ton-vault.png)

## Centralized Part
> The centralized part of the project is represented by the 
> - **Ton Vault Node**
> - **Document-oriented consistent storage ([MongoDB](https://www.mongodb.com/) for instance)** 
> - **Public API gateway**
> 
> Using Public API Gateway, Ton Wallet and official Ton Vault App users can get everything they need to interact with their secrets out of the box.

## Decentralized Part (under development)
> From a bird's eye view this part represents a distributed database of secrets, based on the peer-to-peer (P2P) interaction of nodes. Any participant, if they wish, can launch their own Ton Vault Node and store secrets within it. All data can be synchronized with a public server, provided by the Ton Vault team (a paid feature) or with any other Ton Vault Node.
>
> Ton Vault Node provide a built-in API, so each client has the right to customize the interface (whether web or application) to interact with their personal storage. By default, however, the application will be synchronized with the Public API.
>
> Nodes communicate with each other using the [TON Storage Protocol](https://github.com/.ton-community/ton-docs/tree/main/docs/participate/ton-storage) and an additional encryption layer built entirely upon the user's selected TON Wallet.
> Utilizing this technology, users can exchange data amongst each other safely and securely thereby creating a decentralized cloud.

> Check our [roadmap](roadmap.md) for features that are currently in development.