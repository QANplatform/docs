---
title: 'Writing a smart contract in Python'
description: 'Learn how to write a smart contract in Python.'
---

# Writing a smart contract in Python

::lead
Learn how to write a smart contract in Python.
::

## Prerequisites

::alert{type="note"}
#title
Note:

#content
- Ensure you successfully [set up your dev environment](/testnet/smart-contract/setup/qvmctl).
::

## Limitations

::alert{type="warning"}
#title
Warning: 

#content
The compiler using https://github.com/go-python/gpython as runtime, hence only support partly Python 3.4
::

## Sample contract functionality

The sample contract serves as a demonstration of general QVM logic.

It is capable of:  
- registering users into the database
- storing the last registered user's name in the database
- echoing the previous user's name to STDOUT
- incrementing the total registered user count
- storing above counter in the database

## Constructor logic

While some programming languages do not have explicit support for constructors you are free to implement your own logic for contract initialization after it gets deployed.

Your binary will be invoked with a single "construct" argument.

## Python smart contract sample

::customCodeBlock
```python
import os
import sys

max_user = 100

def getenv(key, deft):
    return os.getenv(key) or deft


def get_int_env(key, deft):
    try:
    return int(getenv(key, ""))
    except Exception:
    return deft


def stdout_writeln(s):
    sys.stdout.write(s + "\n")


def stderr_writeln(s):
    sys.stdout.write(s + "\n")


def constructor():
    global max_user
    initialized = getenv("DB_QVM_INITIALIZED", "unknown")
    if initialized == "true":
    stderr_writeln("contract is already initialized")
    return -1

    stdout_writeln("DBW=QVM_INIT_MAXUSER=%d" % max_user)
    return 0


def initialize():
    global max_user
    initialized = getenv("DB_QVM_INITIALIZED", "unknown")
    if initialized != "true":
        stderr_writeln("contract is not initialized")
        return -1
        max_user = get_int_env("DB_QVM_INIT_MAXUSER", 0)
        return 0


def contract(argv):
    global max_user
    if len(argv) == 2 and argv[1] == "construct":
        sys.exit(constructor())
    else:
        ret = initialize()
        if ret != 0:
            sys.exit(ret)

    if len(argv) == 3 and argv[1] == "register":
        # GET THE CURRENT USER'S NAME OR DEFAULT TO "unknown" IF THIS IS THE FIRST CALL
        previous_name = getenv("DB_USER_CURRENT", "unknown")
        # GET THE TOTAL USER COUNT
        total_user_count = get_int_env("DB_TOTALUSERS", 0)
        if total_user_count + 1 > max_user:
            stdout_writeln("exceeded max user")
            sys.exit(1)

        # WRITE PREVIOUS USER NAME TO STDOUT
        stdout_writeln("OUT=prevname: " + previous_name)

        # UPDATE CURRENT USER NAME BY WRITING IT TO DB
        stdout_writeln("DBW=USER_CURRENT=" + argv[2])

        # STORE USER NAME UNDER A STORAGE SLOT FOR PERSISTENCE (CURRENT GETS OVERWRITTEN ON EACH CALL)
        stdout_writeln("DBW=USER_%d=%s" % (total_user_count, argv[2]))

        # INCREMENT THE TOTAL USER COUNT
        stdout_writeln("DBW=TOTALUSERS=%d" % (total_user_count+1))

        sys.exit(0)

    if len(argv) >= 2:
        stdout_writeln("Wrong CMD: %s" % argv[1])
        sys.exit(1)

    stdout_writeln("Wrong argv!")
    sys.exit(1)


if __name__ == '__main__':
    contract(sys.argv)
```
::

## Save the contract

Open a text editor and save above sample contract as main.py file.
