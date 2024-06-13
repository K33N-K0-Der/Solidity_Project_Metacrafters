# Solidity_Project_Metacrafters
This repository contains a Solidity smart contract for a simple token called MyToken. The contract includes basic functionalities for minting and burning tokens.

## Description
The MyToken contract is designed to demonstrate basic token operations on the Ethereum blockchain. It includes the following features:

Public variables to store details about the token:

Token Name
Token Abbreviation
Total Supply
A mapping to keep track of balances associated with each address.

A mint function to increase the total supply and the balance of a specified address.

A burn function to decrease the total supply and the balance of a specified address, with a check to ensure the balance is sufficient to burn the specified amount.
