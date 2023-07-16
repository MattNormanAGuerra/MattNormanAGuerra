# Create a Token

This Solidity program is a simple to create our own token.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Jaimmy.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

    
   string public TokenName = "Token";
   string public TokenAbbrv = "Toker";
   uint public TotalSupp = 0;
    
   mapping (address =>uint) public balance;
  
   function mint ( address Address, uint Value) public {
      TotalSupp += Value;
      balance[Address] += Value;
   }
   
   function burn ( address Address, uint Value) public {
      if (balance[Address] >= Value) {

      TotalSupp -= Value;
      balance[Address] -= Value;
      }
}
   
}

```

To compile the code, click on the "Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Solidity.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Solidity" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it. First copy your address at the top below the "Account" then paste it on "balance". Click on the mint section paste your id and add value, and then click on the "Burn" section paste your id and click the button contract in the left-hand sidebar to burn the value. Once you done it all it will apear the result of your code
## Authors

Metacrafter Matt

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
