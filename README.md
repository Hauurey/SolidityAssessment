# Solidity Token
This Solidity program is a simple implementation of a token contract that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a foundational example for those new to Solidity and token creation on the Ethereum blockchain.

## Description
This contract, named myToken, is written in Solidity, a programming language for developing smart contracts on the Ethereum blockchain. It provides basic functionality for minting and burning tokens, allowing for the management of token supply and individual balances. This example serves as a stepping stone for more complex token implementations in the future.

## Getting Started
### Executing the Program
To run this program, you can use Remix, an online Solidity IDE. Follow these steps to get started:

Go to the Remix website: https://remix.ethereum.org/.
Create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol).
Copy and paste the following code into the file:
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract myToken {
    string public tokenName = "POKEMON";
    string public tokenAbbrv = "PKMN";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance to burn");
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Ensure the compiler version is set to 0.8.18 (or another compatible version), and then click the "Compile myToken.sol" button.
Once the code is compiled, deploy the contract by clicking on the "Deploy & Run Transactions" tab. Select the myToken contract from the dropdown menu, and then click on the "Deploy" button.
After the contract is deployed, you can interact with it by calling the mint and burn functions. Enter the address and the amount when prompted, and click the respective button to execute the functions.
## Authors
Metacrafter Haurrey

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.
