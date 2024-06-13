# Solidity_Project_Metacrafters
This repository contains a Solidity smart contract for a simple token called MyToken. The contract includes basic functionalities for minting and burning tokens.

## Description
The MyToken contract is designed to demonstrate basic token operations on the Ethereum blockchain. It includes the following features:

1. Public variables to store details about the token:

 -> Token Name

 -> Token Abbreviation

 -> Total Supply

2. A mapping to keep track of balances associated with each address.

3. A mint function to increase the total supply and the balance of a specified address.

4. A burn function to decrease the total supply and the balance of a specified address, with a check to ensure the balance is sufficient to burn the specified amount.

## Code

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the "sender" address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the "sender".
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
    string public tokenName = "BEFIKRA";
    string public tokenAbbrv = "BF";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Not enough tokens");
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
```
## Author

Abhishek Singh
