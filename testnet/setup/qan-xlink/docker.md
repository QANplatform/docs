---
title: 'Install QAN XLINK Docker'
description: 'Learn how to install QAN XLINK post-quantum cross-signer.'
---

# Install QAN XLINK Docker

::lead
Learn how to install QAN XLINK post-quantum cross-signer.
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you succeeded with Step 1. Add testnet to Wallet
- Ensure you [installed Docker](https://docs.docker.com/engine/install/){:target="_blank"} on your desktop. 
::

## What is QAN XLINK? 

QAN XLINK a custom cross-signature protocol. This protocol enables seamless integration of every Ethereum-compatible wallet (such as MetaMask and Trust Wallet) with quantum-resistant signature-capable keypairs.

## Install QAN XLINK with Docker

1. ::customListItem
    **Make sure Docker is running on your device.**

    It is enough if Docker runs in the background.
::
2. **Open Terminal / Command Prompt on your device.**
3. ::customListItem
    **Copy-paste the following command in Terminal/Command Prompt and press Return/Enter key.**

    ::customCodeBlock
    ```sh
    docker pull qanplatform/xlink:testnet
    docker run -d --name=xlink-testnet --restart=always --volume=xlink-testnet:/xlink qanplatform/xlink:testnet
    ```
    ::
::
4. ::customListItem
    **Copy-paste the following command in Terminal/Command Prompt and press Return/Enter key.**

    ::customCodeBlock
    ```sh
    docker logs -f xlink-testnet
    ```
    ::
::
5. ::customListItem
    **Your new address is ready!**
    
    You just generated your new wallet address which has associated QAN XLINK post-quantum keys.

    Done! You should see something similar in the output  (you can safely ignore the low balance alert):
    
    ::customCodeBlock
    ```sh
    Created mnemonic file with a new securely generated mnemonic at /xlink/mnemonic.txt
    xlink initialized for address: 0xfaE0b7ED46f266cF360E52e0C8E33a37AAaa1a81
    insufficient funds on address, waiting 1 minute before re-checking...
    ```
    ::
::

::alert{type="warning"}
#title
Warning:

#content
QAN XLINK will only automatically cross-sign your future transactions in the background using post-quantum cryptography while Docker is running on your device. 
::