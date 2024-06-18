# Solidity Assessment

This project demonstrates the use of basic variable and variable types, functions and types of functions, mapping, and conditional statements. This is a simple program which can help beginners in Solidity to have a grasp of how it works.

## Description

The user will be able to mint their own token with the function mint, provide it a name and abbreviation, along with the total number of supplies. The user can also check the current balance of their tokens. They can also delete tokens with the function burn, and provide a value with how much they would want to destroy tokens. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "New Jeans";
    string public tokenAbbrev = "NWJN";
    uint public totalSupp = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint(address _add, uint _val) public{
        totalSupp += _val;
        balances[_add] += _val;
    }
    // burn function
    function burn(address _add, uint _val) public{
        if(balances[_add]>=_val){
            totalSupp -= _val;
            balances[_add] -= _val;
        }
    }

}

```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the functions "burn", "mint", "balances", "tokenAbbrev", "tokenName", and "totalSupp". 

## Authors

Kristine Garcia

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
