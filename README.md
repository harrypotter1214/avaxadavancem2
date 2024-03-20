
# ERC20 Token Contract


The code you provided is an implementation of an ERC20 token contract in Solidity. Here's a brief description of the contract and its functionalities:

## Description

The ERC20 token contract is an implementation of the ERC20 standard, which defines a set of functions and events for creating and managing fungible tokens. It includes variables such as totalSupply, balanceOf, and allowance to keep track of the token supply, individual balances of addresses, and approved spending amounts, respectively. The contract also defines a set of functions including transfer, approve, and transferFrom to enable token transfers and approvals. Additionally, it includes functions like mint and burn to create and destroy tokens, and a health system represented by the total_health variable, which can be modified using the attack and heal functions. Finally, the contract emits events Transfer and Approval when token transfers and approvals occur.

The Vault contract serves as a secure storage mechanism for tokens. It interacts with the ERC20 token contract to allow users to deposit and withdraw tokens. The contract takes the address of an ERC20 token in its constructor and defines a token variable to store the token contract instance. It maintains a totalSupply variable and a balanceOf mapping to keep track of the shares held by addresses. The contract provides a deposit function that allows users to deposit tokens into the vault. The function calculates the proportionate number of shares based on the deposited amount and the current token balance in the vault, and mints these shares to the sender. The tokens are transferred from the sender's address to the vault using the transferFrom function of the token contract. Similarly, the contract includes a withdraw function to enable users to withdraw tokens from the vault. The function calculates the proportionate amount of tokens based on the shares being withdrawn and transfers these tokens back to the sender's address, while burning the corresponding shares from the sender's balance.

## Getting Started
 
 ### Installing code

 You can clone this repo or download zip file and run it locally or you can run the code on remix 

 Head over to this website: https://remix.ethereum.org/.
 ### Executing the code

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ERC20game.sol). Copy and paste the solidity file into the remix file

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.17" (or above version), and then click on the "Compile ERC20game.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "solidity" contract from the dropdown menu, change the environment to 'Injected provider' and connect your metamask account, and then click on the "Deploy" button.

### Subnet 
 
Follow the below github repository's readme file in order to install avalanche CLI to your Ubuntu or Mac terminal:
 
 [https://docs.avax.network/tooling/cli-guides/install-avalanche-cli](https://github.com/ava-labs/avalanche-cli)

In order to create a subnet, we run -

```
avalanche subnet create mySubnet
```

In order to deploy the created subnet, we run -

```
avalanche subnet deploy mySubnet
```

To connect your subnet to metamask, you will need to :

* Add network manually and enter Name, RPC URL, Token Symbol and Chain ID that you entered while creating the subnet.
* Import account with test tokens by entering the private key that you get from the terminal after you deploy the subnet.

 
## License

This code is licensed under the [MIT](https://choosealicense.com/licenses/mit/) license.See the LICENSE file for more information.


