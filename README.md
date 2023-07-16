Project Title: MyToken - ERC20 Token Implementation

Description:
The MyToken contract is an implementation of the ERC20 token standard on the Ethereum blockchain. It provides functionalities for creating, managing, and transferring tokens. Here's an overview of the project's functionalities:

1. Token Details:
   - The contract stores the name and symbol of the token as public variables.
   - Token holders' balances are tracked using a mapping called `balanceOf`, which associates addresses with their respective token balances.

2. Total Supply:
   - The total supply of tokens is stored as a public variable called `totalSupply`.

3. Events:
   - The contract emits events for important actions:
     - `Transfer`: Triggered when tokens are transferred from one address to another.
     - `Burn`: Fired when tokens are burned or destroyed.
     - `Mint`: Emitted when new tokens are minted and assigned to an address.

4. Contract Owner:
   - The contract has an owner, who can execute specific functions.
   - The `onlyOwner` modifier ensures that only the contract owner can call certain functions.

5. Constructor:
   - The contract is initialized with an initial token supply, provided during deployment.
   - The token name, symbol, and total supply are set in the constructor.
   - The contract owner is assigned as the deployer of the contract.

6. Transfer Function:
   - The `transfer` function allows token holders to transfer tokens to another address.
   - It checks if the sender has a sufficient token balance before performing the transfer.
   - Tokens are deducted from the sender's balance and added to the recipient's balance.
   - The `Transfer` event is emitted to record the transfer.

7. Burn Function:
   - The `burn` function enables token holders to destroy a specified amount of tokens.
   - It verifies if the caller has a sufficient token balance before burning the tokens.
   - The specified amount is deducted from the caller's balance and removed from the total supply.
   - The `Burn` event is emitted to record the burned tokens.

8. Mint Function:
   - The `mint` function allows the contract owner to mint new tokens and assign them to a specified address.
   - Only the contract owner can call this function due to the `onlyOwner` modifier.
   - Tokens are added to the recipient's balance and included in the total supply.
   - The `Mint` event is emitted to record the minted tokens.

The MyToken contract provides a basic ERC20 token implementation with functionalities for token transfers, burning tokens, and minting new tokens. It serves as a foundation for creating and managing custom tokens on the Ethereum blockchain.
