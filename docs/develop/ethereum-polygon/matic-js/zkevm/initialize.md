---
id: initialize-hermez
title: Initialize HermezClient
sidebar_label: Initialize
description: HermezClient allows you to interact with the Polygon zkEVM network.
keywords:
  - docs
  - maticjs
  - polygon
  - hermez client
image: https://wiki.polygon.technology/img/polygon-logo.png
---

MaticJS library also provides **HermezClient** to interact with the Polygon zkEVM network.

```js
import { HermezClient,use } from "@maticnetwork/maticjs"

const hermezClient = new HermezClient();

await hermezClient.init({
    network: <network name>,  // 'testnet'
    version: <network version>, // 'blueberry'
    parent: {
      provider: <parent provider>,
      defaultConfig: {
        from: <from address>
      }
    },
    child: {
      provider: <child provider>,
      defaultConfig: {
        from: <from address>
      }
    }
});
```

Once the `HermezClient` is initialized, you can interact with all available APIs from MaticJS SDK.
