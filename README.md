# MyToken Smart Contract

This Solidity smart contract implements a simple token with minting and burning functionality. The contract keeps track of the total supply and individual balances and allows tokens to be minted and burned.

## Requirements

1. **Public Variables**:
   - `netsupply`: The total supply of tokens.

2. **Mapping**:
   - `balances`: A mapping from addresses to their respective token balances.

3. **Functions**:
   - `mint`: Increases the total supply and the balance of a specified address.
   - `burn`: Decreases the total supply and the balance of a specified address, ensuring that the balance is sufficient before burning.

## Contract Details

### Public Variables

- **`netsupply`** (`uint`): The total supply of tokens in the contract.

### Mapping

- **`balances`** (`mapping(address => uint)`): A mapping from addresses to their respective token balances.

### Functions

#### `mint`

Increases the total supply of tokens and updates the balance of a specified address.

```solidity
function mint(address _address, uint _value) public {
    netsupply += _value;
    balances[_address] += _value;
}
