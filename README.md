# Solidity Assesment
Project that has a mint and burn token function

Description

Metacrafters solidity assesment - ETH PROOF: Beginner EVM Course

A beginner course for how we can understand and apply minting and burning tokens

Getting Started
1. Open https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.26+commit.8a97fa7a.js
2. Create a solidity file with .sol as its filename
3. Copy and paste the code below

//SPDX-License-Identifier: MIT

pragma solidity 0.8.26;

contract MyToken{
    public variables here
    string public tokenName = "Dickson Vecina";
    string public tokenAbbrv = "Token";
    uint public totalSupply = 0;

mapping(address => uint) public balances;
function mint(address _address, uint _value)

public {
        totalSupply += _value;
        balances[_address] += _value;
    }

function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
    

4.Compile and run the project

5.Deploy the project

# HELP 
Note: If 0.8.26 version is having issues for you, try using other versions.

Author

Dickson Vecina

202110060@fit.edu.ph
