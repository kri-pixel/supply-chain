# Supply Chain Management

[![Node.js](https://img.shields.io/badge/Node.js-v14%2B-green)](https://nodejs.org/en/about)
[![React.js](https://img.shields.io/badge/React.js-Framework-lightblue)](https://react.dev/)
[![Solidity](https://img.shields.io/badge/Smart%20Contract-Solidity-orange)](https://soliditylang.org/)
[![MetaMask](https://img.shields.io/badge/Wallet-MetaMask-lightgrey)](https://metamask.io/)
[![Ganache](https://img.shields.io/badge/TestNet-Ganache-red)](https://metamask.io/)
[![Truffle](https://img.shields.io/badge/Deployment-Truffle-purple)](https://archive.trufflesuite.com/docs/truffle/how-to/install/)

## Description
Supply chain is always hard to manage and requires a lot of admistrative machinery. However, when managed with smart contracts using blockchain, a lot of the paperwork is reduced.
Also it leads to an increase in the transparency and helps to build an efficient Root of Trust. Supply-chain-dapp is such an implementation of a supply chain management system which uses blockchain to ensure a transparent and secure transfer of product from the manufacturer to the customer via the online e-commerce websites. 
## Architecture
The smart contract is being written with Solidity which is then compiled, migrated and deployed using Truffle.js on the Gode Testnet blockchain network.The frontend uses Web3.js to communicate with the smart contract and Gode Testnet blockchain network and Meta Musk Wallet is connect to Gode Test Network to do Transaction between each component in Supply .
****
![architecture-supplu-chain](https://github.com/user-attachments/assets/0474b4e5-f2e0-4697-965f-cbad1980d832)


## Supply Chain Flow

![supply-chain-flow](https://github.com/user-attachments/assets/4c078b4c-cef5-4a59-a74d-925bab0b0d54)



## Smart Contract Working Flow


This is a SupplyChain smart contract written in Solidity. The contract models the various roles and stages involved in the supply chain of a pharmaceutical product.

The contract owner is the person who deploys the contract and is the only one who can authorize various roles like retailer, manufacturer, etc.

There are several roles involved in the supply chain of the pharmaceutical product. These include the raw material supplier, manufacturer, distributor, and retailer.

The smart contract stores information about the medicine, such as its name, description, and current stage in the supply chain. There is also a function to show the current stage of a medicine, which can be used by client applications.

The smart contract also stores information about the various players in the supply chain, such as their name, address, and place of operation.

The addRMS(), addManufacturer(), addDistributor(), and addRetailer() functions can be used by the contract owner to add new players to the supply chain.

Overall, this smart contract provides a way to track the various stages of a pharmaceutical product in the supply chain, ensuring transparency and accountability.

##  🔧 Setting up Local Development

### Step1.
## Installation and Setup

* **VSCODE** : VSCode can be downloaded from https://code.visualstudio.com/
* **Node.js** : Download the latest version of Node.js from https://nodejs.org/ and after installation check     Version using terimal: `node -v`.
* **Git** : Download the latest version of Git from the official website at https://git-scm.com/downloads and   check Version using terimal: `git --version`.

* **Ganache** : Download the latest version of Ganache from the official website at https://www.trufflesuite.com/ganache.
* **MetaMask** : can be installed as a browser extension from the Chrome Web Store or Firefox Add-ons store.
  
### Step2.
## Create, Compile & Deploy Smart Contract. 

* Open VScode and open VScode Terimal by Ctrl + ' .
* **Clone Project** Type the following command and press Enter : git clone : `https://github.com/kri-pixel/supply-chain.git`
* **Install truffle** : Type the following command and press Enter: `npm install -g truffle`
* **Install dependencies** : Type the following command and press Enter: `npm i`
* **File structure for  DApp** : 
  
    - **contracts**: This folder contains the Solidity smart contracts for the DApp. The Migrations.sol contract is automatically created by Truffle and is used for managing migrations.

    - **migrations**: This folder contains the JavaScript migration files used to deploy the smart contracts to the blockchain network.

    - **test**: This folder contains the JavaScript test files used to test the smart contracts.

    - **truffle-config.js**: This file contains the configuration for the Truffle project, including the blockchain network to be used and any necessary settings.

    - **package.jso**n: This file contains information about the dependencies and scripts used in the project.

    - **package-lock.json**: This file is generated automatically and contains the exact version of each dependency used in the project.

    - **Client**s: This Folder contains the client-side code, typically HTML, CSS, and JavaScript, can be organized into a client folder.
* **Compile the smart contract** :  In the terminal, use the following command to compile the smart contract: `truffle compile` 
* **Deploy the smart contract** :
   
    * After Compile We Need To Deploy Your Smart Contract on Blockchain. In Our Case We are Using Ganache Which is personal blockchain for Ethereum development, used to test and develop Smart Contracts.

    * Open Ganache and create new WorkSpace. Copy Rpc Server Address.

    * ![ganache-demo](https://github.com/user-attachments/assets/ebbf1bf5-3bde-4bcd-9086-46c42fc6a9d9)

    * The RPC server is used to allow applications to communicate with the Ethereum blockchain and execute smart contract transactions, query the state of the blockchain, and interact with the Ethereum network.

    * Now to add Rcp address in our truffle-config.js and the replace host address and port address with Our Ganache Rcp.
  
    * After Changing RCP address.Open terminal and run this cmd : `truffle migrate`.
    * This Command Will deploye Smart Contract to Blockchain.

### Step 3.
## Run DAPP. 
* Open a second terminal and enter the client folder
  * `cd client`
 
* Install all packages in the package.json file
  * `npm i`
  
* Install Web3 in the package.json file
  * `npm install -save web3`


* Run this Command :
  * `npm`
 
* Run the app 
  * `npm start`

* The app gets hosted by default at port 3000.

### Step 4.
## Connect Meta Musk with Ganache. 

![connect-metamask](https://github.com/user-attachments/assets/c2177ea7-77b7-4189-8c6a-01bfb0a87f41)
1. Start Ganache: Start the Ganache application and make note of the RPC server URL and port number.

1. Connect MetaMask: Open MetaMask in your browser and click on the network dropdown in the top-right corner.
![metamask-demo](https://github.com/user-attachments/assets/e1895e1b-7a46-447d-97b6-03ebfc5fd9d6)
1. Select "Custom RPC" and enter the RPC server URL and port number for your Ganache instance. Click "Save".

1. Import an account: In Ganache, click on the "Accounts" tab and select the first account listed. Click on the "Copy" button next to the "Private Key" field copy the private key.
     ![import-ganache](https://github.com/user-attachments/assets/f9812664-dfcd-45fa-9913-b575ec722ccd)
 2. In MetaMask, click on the three dots in the top-right corner, select "Import Account", and paste the private key into the private key field. Click "Import".
