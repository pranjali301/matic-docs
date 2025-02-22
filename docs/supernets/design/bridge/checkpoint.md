---
id: checkpoint
title: Ensuring Data Integrity through Checkpoint Management
sidebar_label: Ensuring data integrity through checkpoint management
description: "An overview of the checkpointing mechanism of Supernets."
keywords:
  - docs
  - polygon
  - edge
  - bridge
  - fxportal
  - checkpoint
---

This documents provides an overview on how checkpointing works when using the native Supernets bridge.

---

## Introduction

Checkpointing is the process of recording and committing a snapshot of the state of a system at a specific point in time. In the context of blockchain, checkpoints are used to increase security by allowing faster verification of the state of the blockchain without needing to process all transactions from the genesis block. Checkpoints can be used to speed up sync times for new nodes and help prevent certain types of attacks, such as 51% attacks.

## Checkpoints in Supernets

:::info Key points

- The checkpoints are made **by the validators on the childchain** and are committed to the rootchain.
- A checkpoint serves as a snapshot of the childchain state. This snapshot is stored as a Merkle root and **represents the state of the childchain** at that point in time it was created.
- The checkpoint process is important for **ensuring the security of the network** as it enables the rootchain to detect and prevent any potential fraud or malicious activity on the child.

:::

### CheckpointManager

A `CheckpointManager` contract responsible for managing checkpoints in the network.

The checkpoints represent a snapshot of the childchain state, which is periodically checkpointed to the rootchain by the validators.
The checkpoints are used as a reference point for the rootchain to verify the integrity and accuracy of the data on the childchain.

The contract has several functions to facilitate the management of checkpoints, such as submitting a new checkpoint with metadata, verifying signatures, and getting the event root by block number or epoch. The contract also has a mapping to store the checkpoints and the current validator set, and an array to keep track of the checkpoint block numbers.

The contract uses a Merkle tree to efficiently prove the membership of an event in the childchain state. The tree is constructed using the event roots of each checkpoint, and the membership proofs can be verified using the Merkle proofs provided by the users.

The contract also implements a BLS signature scheme to verify the signatures submitted by the validators. The validators' signatures are aggregated, and the contract checks whether the required voting power threshold is met to accept the checkpoint.

<!--
<div align="center">
  <img src="/img/supernets-checkpoint-exit.excalidraw.png" alt="bridge" width="110%" height="40%" />
</div>
-->
<details>
<summary>Details of the checkpoint</summary>

To elaborate, the root of the Merkle tree is a hash value that represents the entire state of the childchain at a specific point in time. This state includes all of the transactions and other changes that have occurred on the childchain up to that point.

When a checkpoint is made, the root of the Merkle tree is included as part of the checkpoint, along with other metadata. This checkpoint is then sent to the rootchain where it is verified and stored by the validators.

Later, when a user wants to verify a particular event or state on the childchain, they can provide a Merkle proof, which is a cryptographic proof that demonstrates the inclusion of a particular event or state in the Merkle tree. The Merkle proof can be verified by the rootchain using the root of the Merkle tree, which was included in the checkpoint.

In short, the root of the Merkle tree is a compact representation of the entire state of the childchain at a specific point in time, which is included in checkpoints and used for verification purposes.

</details>

<!--
<div align="center">
  <img src="/img/supernets-checkpoint.excalidraw.png" alt="bridge" width="110%" height="40%" />
</div>
-->
