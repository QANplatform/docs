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