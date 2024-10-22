---
title: 'Setting up your dev environment'
description: 'Learn how to set up your QAN TestNet dev environment.'
---

# Setting up your dev environment

::lead
Learn how to set up your QAN TestNet dev environment.
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you [installed Docker](https://docs.docker.com/engine/install/){:target="_blank"} on your desktop.
- Ensure you succeeded with Step 1. Add testnet to [MetaMask](/testnet/setup/wallet/metamask)/[Trust Wallet](/testnet/setup/wallet/trust-wallet)/[EVM-compatible Wallet](/testnet/setup/wallet/evm-wallet)
- Ensure you succeeded with Sept 2. [Install QAN XLINK Docker](/testnet/setup/qan-xlink/docker).
- Ensure you succeeded with Step 3. Import private key to [MetaMask](/testnet/setup/import-private-key/metamask)/[Trust Wallet](/testnet/setup/import-private-key/trust-wallet)/[EVM-compatible Wallet](/testnet/setup/import-private-key/evm-wallet) wallet.
- Ensure you succeeded with Step 4. Request [testnet tokens](/testnet/tools/faucet/telegram-faucet)
::

## Installing qvmctl

The qvmctl CLI tool is the swiss knife for interacting with QVM. It can be acquired and easily used through Docker using the following commands:

### Install image

::customCodeBlock
```sh
docker pull qanplatform/qvmctl
```
::

### Verify installation

::customCodeBlock
```sh
docker run --rm qanplatform/qvmctl version
```
::

If everything went correctly the qvmctl version string should be printed on the terminal.

::customCodeBlock
```sh
v0.0.4-46e19631 
```
::
