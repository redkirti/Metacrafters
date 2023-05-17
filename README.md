# Token Creation Contract

This is a simple contract developed on Solidity which creates a new token named Flash and provides functions to mint and burn tokens.

## Contract Details

### Public Variables

- `tokenName`: A string variable that represents the name of the token (e.g., "FLASH").
- `tokenAbbr`: A string variable that represents the abbreviation of the token (e.g., "FLSH").
- `totalSupply`: An unsigned integer variable that holds the total supply of tokens.

### Mapping Variable

- `balances`: A mapping that associates addresses with their corresponding token balances. It maps addresses to unsigned integer values.

### Mint Function

The `mint` function is used to create new tokens. It takes two parameters: `_address` (the address to assign the tokens to) and `_value` (the amount of tokens to create). When called, this function increases the total supply by the specified `_value` and adds the same amount to the balance of the `_address`.

### Burn Function

The `burn` function is used to destroy existing tokens. It takes two parameters: `_address` (the address from which the tokens will be burned) and `_value` (the amount of tokens to burn). This function verifies if the balance of the `_address` is greater than or equal to the specified `_value`. If the condition is met, it subtracts the `_value` from the total supply and reduces the balance of the `_address` by the same amount.

Note that if the condition is not met (i.e., the balance is insufficient), the `burn` function will have no effect.

## Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Flash.sol). Copy and paste the code in Flash.sol into that file.

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "sayHello" function. Finally, click on the "transact" button to execute the function and retrieve the "Hello World!" message.

## Authors

Metacrafter Chris  

## License

This contract is released under the MIT License.
