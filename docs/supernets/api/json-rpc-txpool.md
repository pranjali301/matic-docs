---
id: json-rpc-txpool
title: TxPool
description: "List of TxPool JSON RPC commands for Polygon Edge."
keywords:
  - docs
  - polygon
  - edge
  - json
  - rpc
  - commands
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import {useState} from 'react';

## txpool_content

Returns a list with the exact details of all the transactions currently pending for inclusion in the next block(s), as well as the ones that are being scheduled for future execution only.

<h4><i>Parameters:</i></h4>

None

<h4><i>Example:</i></h4>


````bash
curl  https://rpc-endpoint.io:8545 -X POST -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"txpool_content","params":[],"id":1}'
````

## txpool_inspect

Returns a list with a textual summary of all the transactions currently pending for inclusion in the next block(s), as well as the ones that are being scheduled for future execution only. This is a method specifically tailored to developers to quickly see the transactions in the pool and find any potential issues.

<h4><i>Parameters:</i></h4>

None

<h4><i>Example:</i></h4>

````bash
curl  https://rpc-endpoint.io:8545 -X POST -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"txpool_inspect","params":[],"id":1}'
````

## txpool_status

Returns the number of transactions currently pending for inclusion in the next block(s), as well as the ones that are being scheduled for future execution only.

<h4><i>Parameters:</i></h4>

None

<h4><i>Example:</i></h4>

````bash
curl  https://rpc-endpoint.io:8545 -X POST -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"txpool_status","params":[],"id":1}'
````
