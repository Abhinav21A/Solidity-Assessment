# Solidity-Assessment
Presenting a simple Solidity smart contract that represents a token with necessary functions such as token burning and minting.

## Description
This program is a contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.It demonstrates various concepts taught in the ETH Beginner Course. The contract includes public variables for storing token details, a mapping to associate addresses with balances, a mint function that accepts an address and a value as parameters, and a burn function.

## Getting Started and Code
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Assessment.sol). Copy and paste the following code into the file:
```javascript
// SPDX-License-Identifier: MIT

contract MyToken {

    // public variables here
    string public Token_Name ="ABHINAV";
    string public Token_Abbrev="AA";
    uint public total_Supply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        total_Supply += _value;
        balances[_address] +=_value;
    }

    // burn function
     function burn (address _address, uint _value) public {
      if (balances[_address] >= _value){
        total_Supply -= _value;
        balances[_address] -=_value;
    }
    }

}
```

## Overview
This project aims to provide users with a hands-on grasp of the several ideas covered in the ETH Beginner Course on Solidity. To supplement instruction and highlight important Solidity capabilities like public variables, mappings, minting, and burning functions, this smart contract contains practical examples and implementations.
