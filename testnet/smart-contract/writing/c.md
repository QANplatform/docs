---
title: 'Writing a smart contract in C'
description: 'Learn how to write a smart contract in C.'
---

# Writing a smart contract in C

::lead
Learn how to write a smart contract in C.
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

## C smart contract sample

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

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
    fprintf(stderr, "contract is already initialized\n");
    exit(1);
  }
  printf("DBW=QVM_INIT_MAXUSER=%d\n", maxUser);
}

static void initialize() {
  const char* val = getenv("DB_QVM_INITIALIZED");
  if (val == NULL || strcmp(val, "true") != 0) {
    fprintf(stderr, "contract is not initialized\n");
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
    if (totalUserCount+1 > maxUser) {
      fprintf(stderr, "exceeded max user\n");
      exit(1);
    }
    // WRITE PREVIOUS USER NAME TO STDOUT
    printf("OUT=prevname: %s\n", previousName);
    // UPDATE CURRENT USER NAME BY WRITING IT TO DB
    printf("DBW=USER_CURRENT=%s\n", argv[2]);
    // STORE USER NAME UNDER A STORAGE SLOT FOR PERSISTENCE (CURRENT GETS OVERWRITTEN ON EACH CALL)
    printf("DBW=USER_%d=%s\n", totalUserCount, argv[2]);
    // INCREMENT THE TOTAL USER COUNT
    printf("DBW=TOTALUSERS=%d\n", totalUserCount+1);
    return 0;
  }
  if (argc >= 2) {
    fprintf(stderr, "Wrong CMD: %s\n", argv[1]);
    exit(1);
  }
  fprintf(stderr, "Wrong args!\n");
  exit(1);
}
```

## Save the contract

Open a text editor and save above sample contract as main.c file.
