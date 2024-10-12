---
title: 'QAN API Methods'
description: 'Use APIs to interact with the QAN TestNet.'
---

# QAN API Methods

::lead
Use APIs to interact with the QAN TestNet.
::

Note: Since QANplatform is Ethereum and EVM-compatible all the official Ethereum RPC Methods work.


## Explore QAN API Methods

::tableCard
<table>
<thead>
<tr>
  <th>Name</td>
  <th>Link to</td>
  <th>Function</td>
</tr>
</thead>
<tbody>
  <tr>
    <td>qan_blockNumber</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_blocknumber">https://docs.qanplatform.com/testnet/qan-api-methods/qan_blocknumber</a></td>
    <td>Returns the latest block number of the blockchain.</td>
  </tr>
  <tr>
    <td>qan_call</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_call">https://docs.qanplatform.com/testnet/qan-api-methods/qan_call</a></td>
    <td>Executes a new message call immediately without creating a transaction on the block chain.</td>
  </tr>
  <tr>
    <td>qan_chainId</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_chainid">https://docs.qanplatform.com/testnet/qan-api-methods/qan_chainid</a></td>
    <td>Returns the current network/chain ID, used to sign replay-protected transaction introduced in EIP-155.</td>
  </tr>
  <tr>
    <td>qan_estimateGas</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_estimategas">https://docs.qanplatform.com/testnet/qan-api-methods/qan_estimategas</a></td>
    <td>Returns an estimation of gas for a given transaction.</td>
  </tr>
  <tr>
    <td>qan_feeHistory</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_feehistory">https://docs.qanplatform.com/testnet/qan-api-methods/qan_feehistory</a></td>
    <td>Returns the collection of historical gas information.</td>
  </tr>
  <tr>
    <td>qan_gasPrice</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gasprice">https://docs.qanplatform.com/testnet/qan-api-methods/qan_gasprice</a></td>
    <td>Returns the current gas price on the network in wei.</td>
  </tr>
  <tr>
    <td>qan_getBalance</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getbalance">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getbalance</a></td>
    <td>Returns the balance of the account of given address.</td>
  </tr>
  <tr>
    <td>qan_getBlockByHash</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockbyhash">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockbyhash</a></td>
    <td>Returns information of the block matching the given block hash.</td>
  </tr>
  <tr>
    <td>qan_getBlockByNumber</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockbynumber">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockbynumber</a></td>
    <td>Returns information of the block matching the given block number.</td>
  </tr>
  <tr>
    <td>qan_getBlockReceipts</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockreceipts">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblockreceipts</a></td>
    <td>Returns all transaction receipts for a given block.</td>
  </tr>
  <tr>
    <td>qan_getBlockTransactionCountByHash</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblocktransactioncountbyhash">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblocktransactioncountbyhash</a></td>
    <td>Returns the number of transactions for the block matching the given block hash.</td>
  </tr>
  <tr>
    <td>qan_getBlockTransactionCountByNumber</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblocktransactioncountbynumber">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getblocktransactioncountbynumber</a></td>
    <td>Returns the number of transactions for the block matching the given block number.</td>
  </tr>
  <tr>
    <td>qan_getCode</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getcode">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getcode</a></td>
    <td>Returns the compiled bytecode of a smart contract.</td>
  </tr>
  <tr>
    <td>qan_getFilterChanges</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getfilterchanges">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getfilterchanges</a></td>
    <td>Polling method for a filter, which returns an array of events that have occurred since the last poll.</td>
  </tr>
  <tr>
    <td>qan_getFilterLogs</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getfilterlogs">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getfilterlogs</a></td>
    <td>Returns an array of all logs matching filter with given id.</td>
  </tr>
  <tr>
    <td>qan_getLogs</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getlogs">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getlogs</a></td>
    <td>Returns an array of all logs matching a given filter object.</td>
  </tr>
  <tr>
    <td>qan_getProof</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getproof">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getproof</a></td>
    <td>Returns the account and storage values of the specified account including the Merkle-proof.</td>
  </tr>
  <tr>
    <td>qan_getStorageAt</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getstorageat">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getstorageat</a></td>
    <td>Returns the value from a storage position at a given address.</td>
  </tr>
  <tr>
    <td>qan_getTransactionByBlockHashAndIndex</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyblockhashandindex">https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyblockhashandindex</a></td>
    <td>Returns information about a transaction given a blockhash and transaction index position.</td>
  </tr>
  <tr>
    <td>qan_getTransactionByBlockNumberAndIndex</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyblocknumberandindex">https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyblocknumberandindex</a></td>
    <td>Returns information about a transaction given a block number and transaction index position.</td>
  </tr>
  <tr>
    <td>qan_getTransactionByHash</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyhash">https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionbyhash</a></td>
    <td>Returns the information about a transaction from a transaction hash.</td>
  </tr>
  <tr>
    <td>qan_getTransactionCount</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactioncount">https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactioncount</a></td>
    <td>Returns the number of transactions sent from an address.</td>
  </tr>
  <tr>
    <td>qan_getTransactionReceipt</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionreceipt">https://docs.qanplatform.com/testnet/qan-api-methods/qan_gettransactionreceipt</a></td>
    <td>Returns the receipt of a transaction by transaction hash.</td>
  </tr>
  <tr>
    <td>qan_getUncleCountByBlockHash</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getunclecountbyblockhash">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getunclecountbyblockhash</a></td>
    <td>Returns the number of uncles for the block matching the given block hash.</td>
  </tr>
  <tr>
    <td>qan_getUncleCountByBlockNumber</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_getunclecountbyblocknumber">https://docs.qanplatform.com/testnet/qan-api-methods/qan_getunclecountbyblocknumber</a></td>
    <td>Returns the number of uncles for the block matching the given block number.</td>
  </tr>
  <tr>
    <td>qan_maxPriorityFeePerGas</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_maxpriorityfeepergas">https://docs.qanplatform.com/testnet/qan-api-methods/qan_maxpriorityfeepergas</a></td>
    <td>Get the priority fee needed to be included in a block.</td>
  </tr>
  <tr>
    <td>qan_newBlockFilter</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_newblockfilter">https://docs.qanplatform.com/testnet/qan-api-methods/qan_newblockfilter</a></td>
    <td>Creates a filter in the node, to notify when a new block arrives.</td>
  </tr>
  <tr>
    <td>qan_newFilter</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_newfilter">https://docs.qanplatform.com/testnet/qan-api-methods/qan_newfilter</a></td>
    <td>Creates a filter object, based on filter options, to notify when the state changes (logs).</td>
  </tr>
  <tr>
    <td>qan_newPendingTransactionFilter</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_newpendingtransactionfilter">https://docs.qanplatform.com/testnet/qan-api-methods/qan_newpendingtransactionfilter</a></td>
    <td>Creates a filter in the node to notify when new pending transactions arrive.</td>
  </tr>
  <tr>
    <td>qan_sendRawTransaction</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_sendrawtransaction">https://docs.qanplatform.com/testnet/qan-api-methods/qan_sendrawtransaction</a></td>
    <td>Creates new message call transaction or a contract creation for signed transactions.</td>
  </tr>
  <tr>
    <td>qan_syncing</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_syncing">https://docs.qanplatform.com/testnet/qan-api-methods/qan_syncing</a></td>
    <td>Returns an object with the sync status of the node if the node is out-of-sync and is syncing. Returns null when the node is already in sync.</td>
  </tr>
  <tr>
    <td>qan_uninstallFilter</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_uninstallfilter">https://docs.qanplatform.com/testnet/qan-api-methods/qan_uninstallfilter</a></td>
    <td>Uninstalls a filter with the given filter id.</td>
  </tr>
  <tr>
    <td>qan_xlinkValid</td>
    <td><a href="https://docs.qanplatform.com/testnet/qan-api-methods/qan_xlinkvalid">https://docs.qanplatform.com/testnet/qan-api-methods/qan_xlinkvalid</a></td>
    <td>Returns the xlink validity time of the account of given address.</td>
  </tr>
</tbody>
</table>
::