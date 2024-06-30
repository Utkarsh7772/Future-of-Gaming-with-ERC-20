# Future-of-Gaming-with-ERC-20

##Contract Initialization

The contract is named DegenToken with metadata variables name ("Degen") and symbol ("DGN").
totalSupply tracks the total number of tokens in circulation.
owner stores the address of the contract deployer, who has special permissions.
Redemption_Status stores the status of a redemption operation.

##Mapping and Modifiers

mapping(address => uint) public balanceOf;: Maps addresses to token balances, allowing lookup of balances by address.
modifier onlyOwner(): Restricts access to functions to only the contract owner, ensuring certain operations are privileged.

##Constructor

constructor(uint initialSupply): Initializes the contract with an initial token supply (initialSupply), assigns all tokens to the contract deployer (msg.sender), and sets owner to the deployer's address.

##Token Transfer Functions

transfer(address to, uint Amount): Allows any token holder to transfer tokens (Amount) to another address (to), ensuring valid recipient and sufficient balance.
transferFrom(address from, address to, uint Amount): Allows authorized addresses to transfer tokens from one account (from) to another (to), after approval.

##Token Minting and Burning

mint(address to, uint Amount): Only accessible to the owner, mints new tokens (Amount) to a specified address (to).
burn(uint Amount): Allows any token holder to burn (destroy irreversibly) their own tokens, reducing the total supply.

##Redemption Function

Redeem(uint prizeCost): Allows token holders to redeem tokens (prizeCost) for a prize, updating the Redemption_Status upon successful redemption.

##Usage

Deployment: Deploy this contract to an Ethereum-compatible blockchain using tools like Remix, Truffle, or Hardhat.
Interact: After deployment, interact with the contract to transfer tokens (transfer), mint new tokens (mint), burn existing tokens (burn), or redeem tokens (Redeem).
Security: Ensure that only authorized addresses can perform sensitive operations like minting and burning to maintain token integrity and prevent misuse.
