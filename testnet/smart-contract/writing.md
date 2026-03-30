---
title: 'Writing a smart contract'
description: 'Overview of smart contract samples.'
---

# Writing a smart contract

::lead
Overview of smart contract samples.
::

## Prerequisites

::alert{type="note"}
#title
Note: 

#content
- Ensure you successfully [set up your dev environment](https://docs.qanplatform.com/testnet/smart-contract/setup/qvmctl).
::

## Smart contract samples

::tableCard
<table>
<thead>
<tr>
  <th style="width: 33%">Programming language</th>
  <th>&nbsp;</th>
</tr>
</thead>
<tbody>
<tr>
  <td class="w-1/2">Solidity</td>
  <td>
    Note: Since QANplatform is Ethereum and EVM-compatible, you can write smart contracts in the same way as you do on Ethereum or other EVM-compatible blockchains.
  </td>
</tr>
<tr>
  <td>TypeScript (TS)</td>
  <td>
    <a href="https://docs.qanplatform.com/testnet/smart-contract/writing/typescript">Writing a smart contract in TypeScript (TS)</a>
  </td>
</tr>
<tr>
  <td>C++</td>
  <td>
    <a href="https://docs.qanplatform.com/testnet/smart-contract/writing/cpp">Writing a smart contract in C++</a>
  </td>
</tr>
<tr>
  <td>C</td>
  <td>
    <a href="https://docs.qanplatform.com/testnet/smart-contract/writing/c">Writing a smart contract in C</a>
  </td>
</tr>
<tr>
  <td>Golang (Go)</td>
  <td>
    <a href="https://docs.qanplatform.com/testnet/smart-contract/writing/go">Writing a smart contract in Golang (Go)</a>
  </td>
</tr>
<tr>
  <td>Python</td>
  <td>
    <a href="/testnet/smart-contract/writing/python">Writing a smart contract in Python</a>
  </td>
</tr>
</tbody>
</table>
::

## Why storage slots must be declared upfront

QVM contracts run inside an isolated sandbox environment. Unlike Solidity
contracts, which execute natively on the node and can access storage slots
dynamically at runtime, QVM contracts cannot reach outside the sandbox to
fetch storage values on demand. All storage slots a contract intends to read
must be declared before the transaction is submitted, so the execution layer can
fetch and inject them as environment variables prior to execution.

## How storage slots map to environment variables

Each storage slot name is prefixed with DB_ when exposed inside the contract.  
For example:  

::tableCard
<table>
<thead>
  <tr>
    <th style="width:50%;">Storage Slot Name</th>
    <th style="width:50%;">Environment Variable inside Contract</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>QVM_INIT_MAXUSER</td>
    <td>DB_QVM_INIT_MAXUSER</td>
  </tr>
  <tr>
    <td>TOTALUSERS</td>
    <td>DB_TOTALUSERS</td>
  </tr>
  <tr>
    <td>USER_CURRENT</td>
    <td>DB_USER_CURRENT</td>
  </tr>
</tbody>
</table>
::

## What happens if slots are not declared

If the -r flag is omitted, qvmctl does not create an AccessList for those slots.
The execution layer has no knowledge of which slots to fetch, so all storage reads
inside the contract return empty values. This is a silent failure - the contract
executes without error but operates on empty state.

## How to declare read slots using qvmctl

Use the -r flag followed by a comma-separated list of slot names. Example for a
contract method diag that reads three slots:

::customCodeBlock
```sh
docker run --rm -v "${PWD}:/ws" qanplatform/qvmctl tx -loglevel debug \
  -rpc "https://rpc-testnet.qanplatform.com" \
  -privkey /ws/privkey.hex \
  -r QVM_INIT_MAXUSER,TOTALUSERS,USER_CURRENT \
  <address> diag
```
::

The -r flag instructs qvmctl to: 1. Build an AccessList transaction that
includes the specified storage slots 2. Have the execution layer fetch the current
values of those slots from on-chain storage 3. Inject them as environment
variables (DB_<SLOT_NAME>) before the contract function runs

## Best practice

Review every storage read in your contract source code and ensure all slot names
are listed in the -r flag when calling qvmctl tx. Any slot not listed will appear
as an empty string inside the contract.
