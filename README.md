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

## License

This contract is released under the MIT License.
