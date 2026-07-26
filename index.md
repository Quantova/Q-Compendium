---
title: Introduction to Quantova
description: A high level introduction to Quantova, a post quantum Layer 1 blockchain.
lang: en
---

# Introduction to Quantova

Quantova is a post quantum Layer 1 blockchain. Its cryptography, virtual machine, contract language, and consensus are built on the NIST post quantum standards, so the keys, signatures, finality, and randomness that secure the network are designed to withstand both classical and quantum attack. Quantova is at the testnet stage and has not yet completed external audit.

## Why post quantum

Classical public key cryptography is vulnerable to a sufficiently capable quantum computer. The cryptography in a chain's trust base cannot be swapped out once value depends on it, so a network that will secure long lived value needs post quantum cryptography from genesis. Quantova is built that way.

## The stack

* Q-Crypto. Q-Crypto is Quantova's implementation of the NIST post quantum standards, written against the published FIPS documents. Signatures use ML-DSA-65 under FIPS 204, key exchange uses ML-KEM-768 under FIPS 203, SLH-DSA under FIPS 205 is available as a hash based signature, and hashing uses SHA-3 with SHAKE under FIPS 202. The transport channel uses ChaCha20-Poly1305.
* QORUS consensus. A committee is sampled by sortition each round to attest to a proposed block, and finality is recorded as a single aggregated certificate under ML-DSA-65 authority keys. The committee is bounded, so the work to finalize a block does not grow with the validator set. See [QORUS consensus](/developers/docs/qorus-consensus/).
* The QVM. The [Quantova Virtual Machine](/developers/docs/qvm/) executes compiled containers on a deterministic register machine, with post quantum signature verification, hashing, and Merkle proof checking as native instructions.
* The Quanta language. Contracts are written in [Quanta](/developers/docs/smart-contracts/quanta/) and compiled to QVM containers. Assets are linear resources and authority is a capability, so the compiler catches whole classes of vulnerability, among them reentrancy and unchecked arithmetic, at compile time.

## Core facts

* Addresses are Q1 bech32m, written with a capital Q.
* The asset is QTOV. Its base unit is the Quon, where one QTOV is one million Quon. The testnet asset is TQTOV.
* The gateway is an HTTP POST to `/v1/<method>` with a flat JSON body. See the [gateway reference](/developers/docs/apis/gateway/).
* The client SDK is the QCore family. QCore.rs is the Rust core, QCore.js is published on npm as `@quantovainc/qcore`, and QCore.py is the Python binding.
* The fungible token standard is [QAsset](/developers/docs/standards/qasset/). The non fungible standard is [QCollectible](/developers/docs/standards/qcollectible/).
* The name service is [QNS](/developers/docs/qns/), with domains under a capital Q top level domain such as Jeff.Q.

## Where to go next

* New to the cryptography, start with [post quantum cryptography](/developers/docs/post-quantum-cryptography/).
* Building an app, see [smart contracts](/developers/docs/smart-contracts/) and the [APIs](/developers/docs/apis/).
* Running infrastructure, see [nodes and clients](/developers/docs/nodes-and-clients/).
