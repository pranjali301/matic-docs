---
id: common-methods
title: Miscellaneous Methods
sidebar_label: Miscellaneous
description: Some of the commonly used methods on the Polygon zkEVM network.
keywords:
  - docs
  - maticjs
  - polygon
  - hermez client
image: https://wiki.polygon.technology/img/polygon-logo.png
---

## isDeposited

The `isDeposited` method can be used to check if a deposit has been completed.

```js
const isDeposited = await hermezClient.isDeposited(tx hash);
```

## isDepositClaimable

The `isDepositClaimable` method checks if a deposit can be claimed on the network.

```js
const isDepositClaimable = await hermezClient.isDepositClaimable(tx hash);
```

## isWithdrawExitable

This method checks if the withdrawal process can be exited.

```js
const isWithdrawExitable = await hermezClient.isWithdrawExitable(tx hash);
```

## isExited

```js
const isExited = await hermezClient.isExited(tx hash);
```