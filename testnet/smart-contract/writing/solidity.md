---
title: 'Writing a smart contract in Solidity'
description: 'Learn how to write a smart contract in Solidity.'
---

# Writing a smart contract in Solidity

::lead
Learn how to write a smart contract in Solidity.
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you succesfully [set up your dev environment](/testnet/smart-contract/setup/qvmctl). 
::

## Sample contract functionality

The sample contract serves as a demonstration of general QVM logic.

It is capable of:
- registering users into the database
- storing the last registered user's name in the database
- echoing the previous user's name to STDOUT
- incrementing the total registered user count
- storing above counter in the database

::customCodeBlock
```solidity
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.8.12 <0.9.0;

contract Contract {
    event Stdout(string msg);

    uint64 private MAXUSER = 100;
    uint64 private TOTALUSERS;
    string private USER_CURRENT = "unknown";
    mapping(string => string) private users;

    // register new user
    function register(string memory user) public {
        require(
            TOTALUSERS < MAXUSER,
            "Exceeds max user."
        );
        emit Stdout(string.concat("prevname: ", USER_CURRENT));
        USER_CURRENT = user;
        users[string.concat("USER_", uint2str(TOTALUSERS))] = user;
        TOTALUSERS++;
    }

    function uint2str(uint _i) internal pure returns (string memory _uintAsString) {
        if (_i == 0) {
            return "0";
        }
        uint j = _i;
        uint len;
        while (j != 0) {
            len++;
            j /= 10;
        }
        bytes memory bstr = new bytes(len);
        uint k = len;
        while (_i != 0) {
            k = k-1;
            uint8 temp = (48 + uint8(_i - _i / 10 * 10));
            bytes1 b1 = bytes1(temp);
            bstr[k] = b1;
            _i /= 10;
        }
        return string(bstr);
    }
}
```
::

## Save the contract

Open a text editor and save above sample contract as main.sol file.