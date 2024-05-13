---
title: 'Import private key to Trust Wallet'
description: 'Learn how to add your new wallet which was generated by QAN XLINK to Trust Wallet. '
---

# Import private key to Trust Wallet

::lead
Learn how to add your new wallet which was generated by QAN XLINK to Trust Wallet. 
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you succeeded with Step [1. Add testnet to Wallet to Trust Wallet](/testnet/setup/wallet/trust-wallet)
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

    ```sh
    sudo cp /var/lib/docker/volumes/xlink/_data/privkey* > $HOME/Desktop/privkey.txt
    ```
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

## Import private key to Trust Wallet on desktop

1. **Open Trust Wallet**
2. **Click on 'Settings'.**
3. **Click ‘Manage Wallets'.**
4. **Click 'Add new wallet'.**
5. **Click 'Import or recover wallet'.**
6. **Type in your Trust Wallet password.**
7. **Choose 'I have 24 word Secret Phrase' from the dropdown menu.**
8. **Copy the contents from the file you saved on your Desktop (privkey_0_0xYOURADDR.txt) in the previous step (Get private keys from QAN XLINK) and paste it in the input box of the popup.**
9. **Click the ‘Next’ button to finish the process.**

At this point, the account has been successfully added and is available for use within Trust Wallet. You can add a dedicated name to it as well. 

## Import private key to Trust Wallet on mobile

1. **Open Trust Wallet**
2. **Click on 'Settings' located in the top left corner.**
3. **Click ‘Wallets'.**
4. **Click '+' located in the top right corner.**
5. **Click 'Add existing wallet'.**
6. **Choose 'Secret phrase' from the list.**
7. **Click 'Multi-coin wallet'.**
8. **Copy the contents from the file you saved on your Desktop (privkey_0_0xYOURADDR.txt) in the previous step (Get private keys from QAN XLINK) and paste it in the input box of the popup.**
9. **Click the ‘Restore wallet’ button to finish the process.**

At this point, the account has been successfully added and is available for use within Trust Wallet. 