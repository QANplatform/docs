---
title: 'Writing a smart contract in Golang (Go)'
description: 'Learn how to write a smart contract in Golang (Go).'
---

# Writing a smart contract in Golang (Go)

::lead
Learn how to write a smart contract in Golang (Go).
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

## Golang (Go) smart contract sample

::customCodeBlock
```go
package main

import (
	"fmt"
	"os"
	"strconv"
)

var maxUser int = 100

// $0 construct
func constructor() {
	if os.Getenv("DB_QVM_INITIALIZED") == "true" {
		panic("contract is already initialized")
	}
	os.Stdout.WriteString(fmt.Sprintf("DBW=QVM_INIT_MAXUSER=%s\n", fmt.Sprintf("%d", maxUser)))
}

func initialize() {
	if os.Getenv("DB_QVM_INITIALIZED") != "true" {
		panic("contract is not initialized")
	}
	maxUser, _ = strconv.Atoi(os.Getenv("DB_QVM_INIT_MAXUSER"))
}

func main() {
	if len(os.Args) == 2 && os.Args[1] == "construct" {
		constructor()
		os.Exit(0)
	} else {
		initialize()
	}

	// THIS SAMPLE ONLY SUPPORTS THE "register" FUNCTION
	if len(os.Args) == 3 && os.Args[1] == "register" {

		// GET THE CURRENT USER'S NAME
		previousName := os.Getenv("DB_USER_CURRENT")

		// OR DEFAULT TO "unknown" IF THIS IS THE FIRST CALL
		if len(previousName) == 0 {
			previousName = "unknown"
		}

		// GET THE TOTAL USER COUNT
		totalUserCount, _ := strconv.Atoi(os.Getenv("DB_TOTALUSERS"))
		if totalUserCount+1 > maxUser {
			panic("exceeded max user")
		}

		// WRITE PREVIOUS USER NAME TO STDOUT
		os.Stdout.WriteString(fmt.Sprintf("OUT=prevname: %s\n", previousName))

		// UPDATE CURRENT USER NAME BY WRITING IT TO DB
		os.Stdout.WriteString(fmt.Sprintf("DBW=USER_CURRENT=%s\n", os.Args[2]))

		// STORE USER NAME UNDER A STORAGE SLOT FOR PERSISTENCE (CURRENT GETS OVERWRITTEN ON EACH CALL)
		os.Stdout.WriteString(fmt.Sprintf("DBW=USER_%d=%s\n", totalUserCount, os.Args[2]))

		// INCREMENT THE TOTAL USER COUNT
		os.Stdout.WriteString(fmt.Sprintf("DBW=TOTALUSERS=%d\n", totalUserCount+1))
		os.Exit(0)
	}
	if len(os.Args) >= 2 {
		os.Stderr.WriteString(fmt.Sprintf("Wrong CMD: %s\n", os.Args[1]))
		os.Exit(1)
	}
	os.Stderr.WriteString("Wrong args!\n")
	os.Exit(1)
}
```
::

## Save the contract

Open a text editor and save above sample contract as main.go file.
