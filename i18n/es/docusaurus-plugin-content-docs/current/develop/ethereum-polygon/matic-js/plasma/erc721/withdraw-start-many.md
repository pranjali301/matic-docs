---
id: withdraw-start-many
title: withdrawStartMany
keywords:
- 'plasma client, erc721, withdrawStartMany, polygon, sdk'
description: 'Inicia el proceso de retiro.'
---

El método `withdrawStartMany` se puede utilizar para iniciar el proceso de retiro que quemará los múltiples tokens en la cadena de Polygon.

```
const erc721Token = plasmaClient.erc721(<root token address>);

const result = await erc721Token.withdrawStartMany([<token id1>, <token id2>]);

const txHash = await result.getTransactionHash();

const txReceipt = await result.getReceipt();

```
