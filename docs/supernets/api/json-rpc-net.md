---
id: json-rpc-net
title: Net
description: "List of Net JSON RPC commands for Polygon Edge."
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

## net_version

Returns the current network id.

<h4><i>Parameters:</i></h4>

None

<h4><i>Returns:</i></h4>

* <b> String </b> - The current network id.

<h4><i>Example:</i></h4>

````bash
curl  https://rpc-endpoint.io:8545 -X POST -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"net_version","params":[],"id":83}'
````

## net_listening

Returns true if a client is actively listening for network connections.

<h4><i>Parameters:</i></h4>

None

<h4><i>Returns:</i></h4>

* <b> Boolean </b> - true when listening, otherwise false.

<h4><i>Example:</i></h4>

````bash
curl  https://rpc-endpoint.io:8545 -X POST -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"net_listening","params":[],"id":83}'
````

## net_peerCount

Returns number of peers currently connected to the client.

<h4><i>Parameters:</i></h4>

None

<h4><i>Returns:</i></h4>

* <b> QUANTITY </b> - integer of the number of connected peers.

<h4><i>Example:</i></h4>

````bash
curl  https://rpc-endpoint.io:8545 -X POST -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"net_peerCount","params":[],"id":1}'
````
