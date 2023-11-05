[![Open in Gitpod][gitpod-badge]][gitpod]  [![Foundry][foundry-badge]][foundry] [![License: MIT][license-badge]][license]

[gitpod]: https://gitpod.io/#https://github.com/PaulRBerg/foundry-template
[gitpod-badge]: https://img.shields.io/badge/Gitpod-Open%20in%20Gitpod-FFB45B?logo=gitpod
[foundry]: https://getfoundry.sh/
[foundry-badge]: https://img.shields.io/badge/Built%20with-Foundry-FFDB1C.svg
[license]: https://opensource.org/licenses/MIT
[license-badge]: https://img.shields.io/badge/License-MIT-blue.svg


# Foundry Fund Me



A smart contract written in Foundry







## QuickStart


```
git clone https://github.com/prakhar-kt/foundry-fund-me
cd foundry-fund-me
forge build
```


## Usage

### Deploy

```
forge script script/DeployFundMe.s.sol
```


## Running Tests

There are 4 test tiers:

- Unit
- Integration
- Forked
- Staging

```
    forge test
```

or 
```
    forge test --fork-url $SEPOLIA_RPC_URL
```

### Test Coverage

```
    forge coverage
```


## Deployment to a testnet or mainnet

1. Setup environment variables

Set your SEPOLIA_RPC_URL and PRIVATE_KEY  as environment variables. You can add them to a .env file.

- ```PRIVATE_KEY```: The private key of your account (like from metamask). NOTE: FOR DEVELOPMENT, PLEASE USE A KEY THAT DOESN'T HAVE ANY REAL FUNDS ASSOCIATED WITH IT.

- ```SEPOLIA_RPC_URL```: This is url of the sepolia testnet node you're working with. You can get setup with one for free from [Alchemy](https://www.alchemy.com/)

Optionally, add your ```ETHERSCAN_API_KEY``` if you want to verify your contract on Etherscan.

2. Get testnet ETH

Head over to faucets.chain.link and get some testnet ETH. You should see the ETH show up in your metamask.

3. Deploy

```
forge script script/DeployFundMe.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify --etherscan-api-key $ETHERSCAN_API_KEY
```








## Scripts


After deploying to a testnet or local net, run the Scripts:

Using cast deployed locally example:

```
cast send <FUNDME_CONTRACT_ADDRESS> "fund()" --value 0.1ether --private-key <PRIVATE_KEY>
```
or

```
forge script script/Interactions.s.sol --rpc-url sepolia  --private-key $PRIVATE_KEY  --broadcast
```

Withdraw
```
cast send <FUNDME_CONTRACT_ADDRESS> "withdraw()"  --private-key <PRIVATE_KEY>
```

### Estimate gas

Estimate how much gas things cost by running:
```
forge snapshot
```
And see the output in file called ```.gas-snapshot```



## Formatting

To format the code:
```
forge fmt 
```
## Thank you!


## 🔗 Links

[![Prakhar Srivastava Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/prakharkt)

[![Prakhar Srivastava Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/prakhar-srivastava-5793241a8/)

[![Patrick Collins Medium](https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@psrivasin)


