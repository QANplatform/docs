---
title: 'Import private key to EVM-compatible wallet'
description: 'Learn how to add your new wallet which was generated by QAN XLINK to EVM-compatible wallet. '
---

# Import private key to EVM-compatible wallet

::lead
Learn how to add your new wallet which was generated by QAN XLINK to EVM-compatible wallet. 
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you succeeded with Step [1. Add testnet to Wallet to EVM-compatible wallet](/testnet/setup/wallet/evm-wallet)
- Ensure you succeeded with Step [2. Install QAN XLINK Docker](/testnet/setup/qan-xlink/docker)
::

## Before you start

::alert{type="warning"}
#title
Warning:

#content
- Ensure you have backups of your seed phrase(s) and/or private key(s).
- Ensure you do **NOT** reset your already installed wallet application.
- Ensure you add a new wallet/address to your wallet application for testing.
- Ensure you do **NOT** use your wallet with funds for testing purposes.
- Ensure you never interact with tokens randomly airdropped to your wallet.
::

## Get private keys from QAN XLINK (Linux)

1. ::customListItem
    **Copy the Private key file from the Docker Volume to your desktop with the following command executed in your Terminal:**

    ::customCodeBlock
    ```sh
    docker run --rm -it -v xlink:/xlink:ro alpine sh -c 'cat /xlink/privkey*'
    ```
    ::
::

## Get private keys from QAN XLINK (Windows, macOS)

1. **Open Docker.**
2. **Click ‘Volumes’ located on the left sidebar.**
3. ::customListItem
    **Click ‘xlink’ on the list.**

    After clicking on it, there will be two tabs: "IN USE" and "DATA"
::
4. ::customListItem
    **Click on the "DATA" tab**

    You will see a file with the following name: privkey_0_0xYOURADDR.txt
::
5. ::customListItem
    **Save the file ‘privkey_0_0xYOURADDRESS.txt’ on your desktop.**

    Try to right click the file name and then click ‘Save as...’ if the option appears. 

    If  this doesn’t work then you can see three dots on the right side while hovering over the file name with your mouse, click on the three dots and click ‘Save as...’
::

## Import private key to EVM-compatible wallet

1. **Open EVM-compatible wallet.**
2. **Import a wallet in your application.**
8. **Copy the contents from the file you saved on your Desktop (privkey_0_0xYOURADDR.txt) in the previous step (Get private keys from QAN XLINK) and paste it in the input box of the popup.**
9. **Save the settings.**

At this point, the account has been successfully added and is available for use within your EVM-compatible wallet.