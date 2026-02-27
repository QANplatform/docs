---
title: "Install QAN XLINK Desktop App Beta Version"
description: "Learn how to install the QAN XLINK desktop app."
---

# Install QAN XLINK Desktop App Beta Version

::lead
Learn how to install the QAN XLINK desktop app.
::

Internal testing of our cross-signature protocol is complete, and now it's your turn.

We're opening the QAN XLINK desktop app to community beta testers to put it through its paces in real-world conditions. Your feedback at this stage directly shapes the final release.

## Before you install, keep in mind

This is a beta build, expect rough edges and report anything unexpected.

## Install Beta Desktop App for Windows

**System requirements:**

- Windows 10+ AMD64
- Linux AMD64 (Debian based)

[Download the Beta Desktop App for Windows](https://qanplatform.com/download/xlink/windows){:target="_blank"}

A notification may appear stating 'Windows protected your PC'.

1. Select 'More info'.
2. Click 'Run anyway'."

**How to verify:**

1. Open Power Shell window
2. ::customListItem
    Type this command into the command window:  

    ::customCodeBlock
    ```sh
    CertUtil -hashfile Downloads\qan_xlink_windows_beta_0.46.exe SHA256
    ```
    ::
::
3. Press Enter to run the command. This will present you with an alphanumeric sequence that is called a hash. If this hash is identical to the one listed below then the integrity check passed. 

**SHA256 checksum:** 526acf7c687cbab33033aa749c24a7e0bf0ef6ed8d118a9fe1f0b6d05c7b8f12

## Install Beta Desktop App for Linux

**System requirements:**  
- Linux AMD64 (Debian based)

[Download the Beta Desktop App for Linux](https://qanplatform.com/download/xlink/linux){:target="_blank"}

**How to verify:**

1. Open terminal window
2. ::customListItem
    Type this command into the command window:  

    ::customCodeBlock
    ```sh
    sha256sum "$HOME/Downloads/qan_xlink_linux_beta_0.46"
    ```
    ::
::
3. Press Enter to run the command. This will present you with an alphanumeric sequence that is called a hash. If this hash is identical to the one listed below then the integrity check passed.

**SHA256 checksum:** 5a858d1fd77dca3a6e723d545b9c9a41c828c5b4a12f13cb44560c6dfd6183db

Once you've had a chance to explore, let us know what you find. Bug reports, usability feedback, and feature suggestions are all welcome!

Every submission is reviewed by the team.

[Submit Your Feedback](https://forms.gle/cAbgVKyjPd2XoakN7){:target="_blank"}

Thank you for helping us build something better. Your testing makes the difference.
