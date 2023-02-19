

<h1 align="center">crowdfund-dapp</h1>



## 📺 Quickstart

<div align="center">
  <img src="/crowdfundmantle.jpg" />
</div>

## 🛠️ Installation guide

### ⌛️ create-mantle-dapp command

Open up your terminal (or command prompt) and type the following command:

```sh
npx create-mantle-dapp <your-dapp-name>

# cd into the directory
cd <your-dapp-name>
```

### 🔑 Private key

Ensure you create a `.env` file in the `root` directory. Then paste your [Metamask private key](https://metamask.zendesk.com/hc/en-us/articles/360015289632-How-to-export-an-account-s-private-key) in `.env` with the variable name `PRIVATE_KEY` as follows:

```sh
PRIVATE_KEY=1234
```

### ⚙️ Compile

Now, you can write your contracts in `./contracts/` directory, replace `Greeter.sol` with `<your-contracts>.sol` file. To write tests, go to `./test` directory and create `<your-contracts>.test.js`.

```sh
npx hardhat compile

# for testing the smart contracts
npx hardhat test
```

After successful compilation, the artifacts directory will be created in `./src/artifacts` with a JSON `/contracts/<your-contracts>.sol/<your-contracts>.json` containing ABI and Bytecode of your compiled smart contracts.

Please make the changes while [Importing](https://github.com/akhileshthite/create-mantle-dapp/blob/e0ba9b3bf48552725cef54a0d4ef5557d600e981/src/App.js#L8) the JSON in `./src/app.js`.

### ⛓️ Deploy

Before deploying the smart contracts, please make sure you have a `mantle testnet` in your Metamask wallet with sufficient funds, follow this [quickstart](https://docs.mantle.xyz/introducing-mantle/quick-start) guide if you do not have one.

Also, make changes in `./scripts/deploy.js` (replace the greeter contract name with `<your-contract-name>`).

For deploying the smart contracts to Mantle network, type the following command:

```sh
npx hardhat run --network mantle_testnet scripts/deploy.js
```

Copy-paste the deployed contract address [here](https://github.com/akhileshthite/create-mantle-dapp/blob/e0ba9b3bf48552725cef54a0d4ef5557d600e981/src/App.js#L31)

```sh
<your-contract> deployed to: 0x...
```

### 💻 React client

start react app

```sh
npm start
# Starting the development server...
```

Please read the [hardhat documentation](https://hardhat.org/hardhat-runner/docs/getting-started#quick-start) and [mantle documentation](https://www.mantle.xyz/developers) for more details.

