---
id: deposit-many
title: depositMany
keywords:
- 'pos client, erc721, depositMany, polygon, sdk'
description: 'Deposita token multipli da ethereum alla catena di polygon.'
---

Il metodo `depositMany` può essere utilizzato per depositare più token da ethereum alla catena di polygon.

```
const erc721RootToken = posClient.erc721(<root token address>, true);

const result = await erc721RootToken.depositMany([<token id1>,<token id2>], <user address>);

const txHash = await result.getTransactionHash();

const txReceipt = await result.getReceipt();

```
