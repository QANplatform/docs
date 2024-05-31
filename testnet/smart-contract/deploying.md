---
title: 'Deploying a smart contract'
description: 'Learn how to deploy a smart contract.'
---

# Deploying a smart contract

::lead
Learn how to deploy a smart contract.
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure your succesfully saved you previously written contract. 
::

## Run the deploy command of qvmctl using docker

```sh
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v $(pwd):/ws qanplatform/qvmctl deploy -language golang -privkey /ws/privkey -rpc <testnet_endpoint> </path/to/sourcecode>
```

## Notes for solidity

- The compiler does not support dynamic imports out of the box. It might be enabled later, but we generally recommend to have all sources in a single file to be absolutely sure what is being deployed.
- Also, since Solidity also supports multiple contracts during compile, you must specify which contract you want to deploy with an extra parameter like this:

```sh
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v $(pwd):/ws qanplatform/qvmctl deploy -language solidity -solidity.name MyContract -privkey /ws/privkey -rpc <testnet_endpoint> </path/to/sourcecode>
```

Where -solidity.name **MyContract** refers to the name of the contract you want to deploy.