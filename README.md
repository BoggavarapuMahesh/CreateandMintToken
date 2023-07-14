# CreateandMintToken
# A new token is created on the local HardHat network
 the creation of a new token on the local HardHat network. When deploying the contract, you provide the token's name, symbol, and initial total supply. This initializes the token with the specified details and assigns the total supply to the contract owner.
 
# The contract includes three events:

Transfer event is emitted when tokens are transferred from one address to another.
Burn event is emitted when tokens are burned, i.e., destroyed or removed from circulation.
Mint event is emitted when new tokens are created and assigned to an address.

The constructor function constructor is executed only once during contract deployment. It initializes the token's name, symbol, and totalSupply. It assigns the total supply to the contract owner's address and sets the owner variable. 

# Mint tokens
Only the contract owner can mint new tokens. The mint function can be called by the owner, passing the address to which the tokens should be minted and the amount to be minted. This function increases the balance of the recipient address and the total supply of tokens. It emits a Mint event to indicate that tokens have been created.
# transfer tokens 
 Any user can transfer tokens to another address using the transfer function. The user needs to specify the recipient address and the amount of tokens to transfer. This function verifies if the sender has enough tokens, deducts the transferred amount from the sender's balance, adds it to the recipient's balance, and emits a Transfer event.

 # Burning Tokens
 Any user can burn (destroy) their own tokens using the burn function. The user specifies the amount of tokens to burn. This function checks if the caller has a sufficient balance, deducts the burned amount from the caller's balance, decreases the total supply of tokens, and emits a Burn event to indicate that tokens have been destroyed.
 
 The contract allows the contract owner to mint new tokens, while any user can transfer or burn tokens they own. This functionality enables the creation, transfer, and destruction of tokens on the local HardHat network.
