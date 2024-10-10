# Solidity Creating Token

This project mints and burns tokens.

## Description

This is an assessment given by MetaCrafters under the ETH PROOF: Beginner EVM Course.

## Getting Started

### Executing program

Follow these steps to execute the program:

1. Open [Remix](https://remix.ethereum.org/).
2. Create a new Solidity file with a `.sol` extension.
3. Copy and paste the following code into the created file:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyToken {

    // public variables here
    string public tokenName = "Dickson Vecina";
    string public tokenAbbrv = "DV";
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
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```
* Compile the project and make sure to select 0.8.26 as the version of the compiler.
* Deploy the project
  
## Help

### Common Problems
* MIT license not specified.
```
// SPDX-License-Identifier: MIT
```
* Incorrect solidity version.
```
pragma solidity 0.8.18;
```
* Correct solidity version.
```
pragma solidity 0.8.26;
```

## Authors
Contributors' names and contact info:
[202110060@fit.edu.ph] (https://github.com/Yosoo-12)
