---
title: 'Introducing the QAN XLINK Desktop App (Beta)'
description: 'Explore the user guide to learn how to use the QAN XLINK desktop app.'
---

# Introducing the QAN XLINK Desktop App (Beta)

Explore the user guide to learn how to use the QAN XLINK desktop app.

::alert{type="note"}
#title
Note: 

#content
Before you download, keep in mind that this is a beta build, expect rough edges and report anything unexpected.
::

## Download Beta Desktop App for Windows

You can download the application [here](https://qanplatform.com/download/xlink/windows){:target="_blank"}.

**System requirements:**
- Windows 10+ AMD64
- Linux AMD64 (Debian based)

A pop-up window may appear saying that 'Windows protected your PC'.

1. Select 'More info'.
2. Click 'Run anyway'."

**How to validate your download before running the app:**

1. Open Power Shell window
2. ::customListItem
    Type this command into the command window:

    ::customCodeBlock
    ```sh
    CertUtil -hashfile Downloads\qan_xlink_windows_beta_0.47.exe
    ```
    ::
::

3. Press Enter to run the command. This will present you with an alphanumeric sequence that is called a hash. If this hash is identical to the one listed below then the integrity check passed.

**SHA256 checksum:** 69adac42cf0e627dbf1db993aa5c3d5954211652700e7453db5e9528b77449e8

## Download Beta Desktop App for Linux

You can download the application [here](https://qanplatform.com/download/xlink/linux){:target="_blank"}

**System requirements:**
- Linux AMD64 (Debian based)
- Download the Beta Desktop App for Linux

**How to validate your download before running the app:**
1. Open terminal window
2. ::customListItem
    Type this command into the command window:
    
    ::customCodeBlock
    ```sh
    sha256sum "$HOME/Downloads/qan_xlink_linux_beta_0.47"
    ```
    ::
::

3. Press Enter to run the command. This will present you with an alphanumeric sequence that is called a hash. If this hash is identical to the one listed below then the integrity check passed.

**SHA256 checksum:** c9ea1add07df421e19c90be8027d63a1ea86a8c99dc28870fce55ee49d5eb61d

## How to use QAN XLINK Desktop Applicaton

### Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you have downloaded the QAN XLINK application on your desktop. 
- Docker is not needed for the QAN XLINK Desktop Application.
::

### What is QAN XLINK?

QAN XLINK is a protocol that seamlessly integrates with existing Ethereum-compatible wallets like MetaMask and Trust Wallet, enabling quantum-safe "designated survivor" keys to be used once Elliptic Curve Cryptography becomes obsolete in practice. Utilizing NIST's primary-recommended lattice-based Post-Quantum Cryptography (PQC) algorithm (ML-DSA, FIPS 204), QAN XLINK provides a 100%-guaranteed safe migration path for the post-quantum era ensuring security even after "Q-Day."

## User Guide

### 1. Initial Setup & Terms of Use

After the application launches, follow these steps:

1. Click "Get started" to begin.
2. Scroll down and check the "I agree..." checkbox to accept our Terms of Use.

### 2. Wallet Creation & Wallet Import

::alert{type="note"}
#title
Note:

#content
If you want to erase your wallet from the app, you'll need to delete the xlink_storage.b64 file. This file contains the encrypted data for your current wallet and is typically stored in the same directory as the application itself.
::

**A, Creating a New QAN XLINK Wallet**

::alert{type="note"}
#title
Note:

#content
- If you forgot your password, there is no technical way to recover it. You'll need to import your wallet again.
- If you forget your Secret Recovery Phrase, there is no way to recover your wallet if you lose access.
::

You will proceed through the following steps:

**Step 1: Password Creation**

1. Click "Create a new QAN XLINK wallet" on the "Let's get started!" screen.
2. Enter your desired password. It must be at least 8 characters long. A strong password is 	recommended for better account protection.
3. Check the box to confirm that you acknowledge full responsibility for managing your password.
4. Click on "Create password".

If your password is deemed weak, a popup will appear. You can click "Use anyway" to continue with a weaker password.

**Step 2: Secret Recovery Phrase**

1. Click the "Tap to reveal" dark gray box to reveal your Secret Recovery Phrase.
2. Carefully save your Secret Recovery Phrase. This is crucial for recovering your wallet if you lose access.
3. Click "Continue".

**Step 3: Secret Recovery Phrase Confirmation**

A, Drag and drop the words in the correct order to confirm your Secret Recovery Phrase.
1. Click a word again to remove it if you make a mistake.
2. Click "Continue" when you've completed ordering the words..
	
B, Alternatively, you can skip the confirmation for testing purposes.
1. Click "Continue without confirmation for testing".
2. Check the box in the popup and click "Skip".

At this point, the process is finalized and an xlink_storage.b64 file is created, containing encrypted data.

**B, Importing a QAN XLINK Wallet**

::alert{type="note"}
#title
Note:

#content
You can import any wallet that uses a 24-word seed phrase.
::

To import an existing wallet:

1. Enter your Secret Recovery Phrase.
2. Click "Continue".
3. ::customListItem
    You will be brought to the password creation step (Step 1 from wallet creation), where you can set a password for this wallet:
  	1. Enter your desired password (at least 8 characters).
	2. Check the box to confirm that you acknowledge full responsibility for managing your password.
  	3. Click "Create password".
::

### 3. Wallet Ready!

Press "Done" to continue to the main screen.

### 4. Adding a Network

::alert{type="note"}
#title
Note:

#content
Currently, only the QAN TestNet network will work within the XLINK app.
::

You can choose from a list of pre-defined networks, or add a custom network.

**A, Choosing a Pre-defined Network:**

The QAN TestNet is available only as a pre-defined network. Simply click on QAN TestNet to add it as your selected network.

**B, Adding a QAN TestNet as Custom Network:**

If you want to add manually, enter the following settings:
- Network name: QAN TestNet
- New RPC URL: https://rpc-testnet.qanplatform.com
- Chain ID: 1121

Once you've entered the desired settings, click "Save Network".

### 5. Main Screen & Account Management

::alert{type="note"}
#title
Note: 

#content
Refresh the application to see updated account statuses, especially after a transfer.
::

**Account Status:**

The main screen shows the status of each of your accounts:

- Protected: Indicates a valid and active connection.
- Not eligible: Your wallet's balance for this account is currently below 1 QANX.
- Error: Check your internet connection.
- Expired: The 24-hour protection period for this account has ended.

**Additional Options:**

- Show Less/Show More (Account): Use this functionality to see more or less account.
- Network Management: Manage your configured networks by clicking the "..." icon in the upper right corner.

### 6. Account Validation & Auto-Renewal

::alert{type="note"}
#title
Note:

#content
If the 24-hour validation window expires, your wallet remains secure, but you will need to re-validate the account to make transactions. The re-validation happens automatically when you launch the app, as long as an internet connection is available.
::

QAN XLINK maintains a cryptographically provable link between Elliptic Curve (EC) secp256k1 and Post-Quantum (PQ) ML-DSA-65 keys. This allows users to continue utilizing EC cryptography while ensuring a seamless migration path to PQ cryptography when necessary. 

**Transaction Signing & Validation Window:**

When a transaction is signed by a wallet and gets broadcasted to the QAN TestNet, the recipient QAN TestNet node will verify whether the wallet is currently cross-signed by QAN XLINK. 

The QAN XLINK  cross-signature is valid for a period of 24 hours from the last time the previous one was submitted. This 24-hour window represents the period during which external applications (MetaMask, Trust Wallet etc.) remain ready to sign new transactions.

**Automatic Re-validation Process:**

To maintain continuous transaction usability within the 24-hour window, the XLINK application automatically re-validates protected accounts while open and connected to the internet. This process generates new ML-DSA-65 signatures:

- Each time the XLINK application is opened and connected to the internet, the account is re-validated.
- Halfway through the 24-hour window (after 12 hours), the application automatically re-validates protected accounts if it remains open and connected to the internet.

**Impact of Offline/Inactivity:**

If the XLINK application is closed or disconnected from the internet for more than 24 hours after the last re-validation, a new re-validation is required before new transactions can be signed. Opening and connecting the application automatically triggers this re-validation process.

### 7. Password Protection

After you've successfully added and reached the "Ready" screen at least once, the application will require your password each time you open it.

### 8. How to remove QAN XLINK

To completely remove the QAN XLINK application, delete both the application itself and the xlink_storage.b64 file (if you created or imported a wallet)
