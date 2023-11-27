# CSE 598: Decentralized Housing Auction Marketplace
## Description
This repository contains the Soldity, JavaScript, and HTML/CSS code for a Auction Decentralized Application for deployment on the Ethereum blockchain.


## Folder Structure
The important folders in the directory include:
- `contracts`: Contains the code for the Auction smart contract
- `documents`: Contains the executive summary and detailed set up instructions
- `migrations`: Contains the JavaScript scripts to deploy and run migrations (adapted from the tutorial)
- `src`: Contains the JavaScript and HTML/CSS for the front end, as well as the code that enables interaction with the smart contract
- `test`: Contains the unit tests for the smart contract

## Instructions for Local Deployment
1. Download the prerequisites to run the application: Truffle IDE, Ganache, NodeJS, MetaMask
2. Run Ganache, and connect MetaMask to Ganache. Detailed instructions for this step can be found in Sections 3.1 and 3.2 in `documents/setup_instructions.pdf`
3. Clone the repo
4. Migrate to root folder of the repo
5. If you would like to reinitialize the app (if for example, you used this application in the past), you will need to delete any `.json` files in `build/contracts`
6. Test the contract functions using unit tests specified in `test/TestAuction.sol` (not essential)
```
$ truffle test
```
7. Compile the contracts `Auction.sol` and `Migrations.sol` located in `contracts/`
```
$ truffle compile
```
8. Migrate the contract to your local server through Ganache. The contract needs to be compiled (Step 7) before it can be migrated
```
$ truffle migrate
```
9. Run the local server
```
$ npm run dev
```

**Note:** Steps 6/7 will create a new folder directory `build/contracts` with `.json` files for the smart contract `Auction.sol` and `Migrations.sol`. These `.json` files contain the "contract" information used to run the app locally