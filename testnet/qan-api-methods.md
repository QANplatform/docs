---
title: 'QAN API Methods'
description: 'Use APIs to interact with the QAN TestNet.'
---

# QAN API Methods

::lead
Use APIs to interact with the QAN TestNet.
::

::alert{type="note"}
#title
Note:

#content
Since QANplatform is Ethereum and EVM-compatible all the official Ethereum RPC Methods work.
::

## Explore QAN API Methods

::tableCard
<table>
<thead>
<tr>
  <th>Name</td>
  <th>Function</td>
</tr>
</thead>
<tbody>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_blocknumber">qan_blockNumber</a></td>
    <td>Returns the latest block number of the blockchain.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_call">qan_call</a></td>
    <td>Executes a new message call immediately without creating a transaction on the block chain.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_chainid">qan_chainId</a></td>
    <td>Returns the current network/chain ID, used to sign replay-protected transaction introduced in EIP-155.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_estimategas">qan_estimateGas</a></td>
    <td>Returns an estimation of gas for a given transaction.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_feehistory">qan_feeHistory</a></td>
    <td>Returns the collection of historical gas information.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gasprice">qan_gasPrice</a></td>
    <td>Returns the current gas price on the network in wei.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getbalance">qan_getBalance</a></td>
    <td>Returns the balance of the account of given address.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockbyhash">qan_getBlockByHash</a></td>
    <td>Returns information of the block matching the given block hash.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockbynumber">qan_getBlockByNumber</a></td>
    <td>Returns information of the block matching the given block number.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockreceipts">qan_getBlockReceipts</a></td>
    <td>Returns all transaction receipts for a given block.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblocktransactioncountbyhash">qan_getBlockTransactionCountByHash</a></td>
    <td>Returns the number of transactions for the block matching the given block hash.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblocktransactioncountbynumber">qan_getBlockTransactionCountByNumber</a></td>
    <td>Returns the number of transactions for the block matching the given block number.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getcode">qan_getCode</a></td>
    <td>Returns the compiled bytecode of a smart contract.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getfilterchanges">qan_getFilterChanges</a></td>
    <td>Polling method for a filter, which returns an array of events that have occurred since the last poll.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getfilterlogs">qan_getFilterLogs</a></td>
    <td>Returns an array of all logs matching filter with given id.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getlogs">qan_getLogs</a></td>
    <td>Returns an array of all logs matching a given filter object.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getproof">qan_getProof</a></td>
    <td>Returns the account and storage values of the specified account including the Merkle-proof.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getstorageat">qan_getStorageAt</a></td>
    <td>Returns the value from a storage position at a given address.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyblockhashandindex">qan_getTransactionByBlockHashAndIndex</a></td>
    <td>Returns information about a transaction given a blockhash and transaction index position.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyblocknumberandindex">qan_getTransactionByBlockNumberAndIndex</a></td>
    <td>Returns information about a transaction given a block number and transaction index position.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyhash">qan_getTransactionByHash</a></td>
    <td>Returns the information about a transaction from a transaction hash.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactioncount">qan_getTransactionCount</a></td>
    <td>Returns the number of transactions sent from an address.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionreceipt">qan_getTransactionReceipt</a></td>
    <td>Returns the receipt of a transaction by transaction hash.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getunclecountbyblockhash">qan_getUncleCountByBlockHash</a></td>
    <td>Returns the number of uncles for the block matching the given block hash.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getunclecountbyblocknumber">qan_getUncleCountByBlockNumber</a></td>
    <td>Returns the number of uncles for the block matching the given block number.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_maxpriorityfeepergas">qan_maxPriorityFeePerGas</a></td>
    <td>Get the priority fee needed to be included in a block.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_newblockfilter">qan_newBlockFilter</a></td>
    <td>Creates a filter in the node, to notify when a new block arrives.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_newfilter">qan_newFilter</a></td>
    <td>Creates a filter object, based on filter options, to notify when the state changes (logs).</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_newpendingtransactionfilter">qan_newPendingTransactionFilter</a></td>
    <td>Creates a filter in the node to notify when new pending transactions arrive.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_sendrawtransaction">qan_sendRawTransaction</a></td>
    <td>Creates new message call transaction or a contract creation for signed transactions.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_syncing">qan_syncing</a></td>
    <td>Returns an object with the sync status of the node if the node is out-of-sync and is syncing. Returns null when the node is already in sync.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_uninstallfilter">qan_uninstallFilter</a></td>
    <td>Uninstalls a filter with the given filter id.</td>
  </tr>
  <tr>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_xlinkvalid">qan_xlinkValid</a></td>
    <td>Returns the xlink validity time of the account of given address.</td>
  </tr>
</tbody>
</table>
::