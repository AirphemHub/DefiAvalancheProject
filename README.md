# Defi Avalanche Project
A simple example of ERC20 token implementation and a Vault contract for managing deposits and withdrawals of the token.

### Description
This project consists of two Solidity contracts:
1. ERC20: A basic implementation of the ERC20 token standard.
2. Vault: A contract that allows users to deposit ERC20 tokens and receive shares in return. Users can also withdraw their tokens by burning their shares.

The ERC20 contract includes functions for transferring tokens, approving allowances, minting new tokens, and burning existing tokens. The Vault contract allows users to deposit tokens in exchange for shares, and withdraw tokens by burning their shares.

### Getting Started
#### Installing
1. Clone the repository:
    ```git clone https://github.com/AirphemHub/DefiAvalancheProject.git```
2. Navigate to the project directory:
    ```cd DefiAvalancheProject```

#### Executing program
To deploy and interact with the contracts, follow these steps:
1. Compile the contracts using a Solidity compiler (e.g., solc or through an IDE like Remix).
2. Deploy the ERC20 contract first.
3. Deploy the Vault contract, passing the address of the deployed ERC20 contract to its constructor.
4. Use the following commands to interact with the contracts:

#### Deploying ERC20 Contract
    ```
        // Deploy ERC20 contract
        ERC20 erc20 = new ERC20();
    ```
#### Deploying Vault Contract
    ```
        // Deploy Vault contract with the address of the ERC20 token
        Vault vault = new Vault(address(erc20));
    ```
#### Interacting with the ERC20 Contract
    ```
        // Mint tokens
        erc20.mint(1000);

        // Transfer tokens
        erc20.transfer(address(vault), 100);
    ```
#### Interacting with the Vault Contract
    ```
        // Deposit tokens into the Vault
        vault.deposit(100);

        // Withdraw tokens from the Vault
        vault.withdraw(50);
    ```

### Help
For common issues or troubleshooting:
- Ensure that the ERC20 contract is deployed before deploying the Vault contract.
- Make sure to approve the Vault contract to spend your tokens if you're transferring tokens from a different address.

### Authors
Oluwafemi Shobowale
@[AirphemHub](https://github.com/AirphemHub)

### License
This project is licensed under the MIT License - see the LICENSE.md file for details.





