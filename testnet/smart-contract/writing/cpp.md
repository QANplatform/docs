---
title: 'Writing a smart contract in C++'
description: 'Learn how to write a smart contract in C++.'
---

# Writing a smart contract in C++

::lead
Learn how to write a smart contract in C++.
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

## Constructor logic

While some programming languages do not have explicit support for constructors you are free to implement your own logic for contract initialization after it gets deployed. 

Your binary will be invoked with a single “construct” argument. 

## C++ smart contract sample

::customCodeBlock
```cpp
#include <iostream>
#include <cstdlib>
#include <cstring>

using namespace std;

// Copied from C version
static int envAtoi(const char* env) {
  const char* val = getenv(env);
  if (val == NULL) {
    return 0;
  }
  return atoi(val);
}

int maxUser = 100;

static void construct() {
  const char* val = getenv("DB_QVM_INITIALIZED");
  if (val && strcmp(val, "true") == 0) {
    cerr << "contract is already initialized" << endl;
    exit(1);
  }
  cout << "DBW=QVM_INIT_MAXUSER=" << maxUser << endl;
}

static void initialize() {
  const char* val = getenv("DB_QVM_INITIALIZED");
  if (val == NULL || strcmp(val, "true") != 0) {
    cerr << "contract is already not initialized" << endl;
    exit(1);
  }
  maxUser = envAtoi("DB_QVM_INIT_MAXUSER");
}

int main(int argc, char *argv[]) {
  if (argc == 2 && strcmp(argv[1], "construct") == 0) {
    construct();
    exit(0);
  }
  // THIS SAMPLE ONLY SUPPORTS THE "register" FUNCTION
  if (argc == 3 && strcmp(argv[1], "register") == 0) {
    initialize();
    // GET THE CURRENT USER'S NAME
    const char *previousName = getenv("DB_USER_CURRENT");
    // OR DEFAULT TO "unknown" IF THIS IS THE FIRST CALL
    if (previousName == NULL || strlen(previousName) == 0) {
      previousName = "unknown";
    }
    // GET THE TOTAL USER COUNT
    int totalUserCount = envAtoi("DB_TOTALUSERS");
    // WRITE PREVIOUS USER NAME TO STDOUT
    cout << "OUT=prevname: " << previousName << endl;
    // UPDATE CURRENT USER NAME BY WRITING IT TO DB
    cout << "DBW=USER_CURRENT=" << argv[2] << endl;
    // STORE USER NAME UNDER A STORAGE SLOT FOR PERSISTENCE (CURRENT GETS OVERWRITTEN ON EACH CALL)
    cout << "DBW=USER_" << totalUserCount << "=" << argv[2] << endl;
    // INCREMENT THE TOTAL USER COUNT
    cout << "DBW=TOTALUSERS=" << totalUserCount+1 << endl;
    return 0;
  }
  if (argc >= 2) {
    cerr << "Wrong CMD: " << argv[1] << endl;
    exit(1);
  }
  cerr << "Wrong args!" << endl;
  exit(1);
}
```
::

## Save the contract

Open a text editor and save above sample contract as main.cpp file.
