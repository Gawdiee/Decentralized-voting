Decentralized Voting Application
This is a decentralized voting application built with React and Ethereum smart contracts. It allows users to connect their MetaMask wallet, view a list of candidates, and cast votes on the Ethereum blockchain. The application displays the remaining voting time, candidate vote counts, and restricts users to a single vote.
Features

Connect to MetaMask for secure Ethereum wallet integration
View real-time candidate list with vote counts
Cast a vote for a candidate using a smart contract
Display voting status and remaining time
Prevent duplicate voting per account
Responsive UI with clean design

Prerequisites

Node.js (v14 or higher)
MetaMask browser extension
Ethereum client (e.g., Hardhat, Ganache) for local development
Ethers.js for Ethereum interaction
React (v17 or higher)

Installation

Clone the repository:
git clone <repository-url>
cd <repository-folder>


Install dependencies:
npm install


Set up a local Ethereum network (e.g., Hardhat):
npx hardhat node


Deploy the smart contract:
npx hardhat run scripts/deploy.js --network localhost


Update the contract address in src/Constant/constant.js with the deployed contract address.

Start the React application:
npm start



Usage

Open the application in a browser with MetaMask installed.
Click "Login Metamask" to connect your wallet.
View the list of candidates and their current vote counts.
Enter the candidate index and click "Vote" to cast your vote.
If you have already voted, the interface will display a message indicating so.
The remaining voting time is displayed, and voting is disabled once the time expires.

Project Structure

public/: Static assets and HTML template
index.html: Main HTML file
robots.txt: Crawler configuration


src/: React application source code
App.js: Main React component
App.css: Styles for the application
Components/: React components for Login, Connected, and Finished states
Constant/constant.js: Smart contract ABI and address
index.js: React entry point
reportWebVitals.js: Performance monitoring
setupTests.js: Jest testing configuration


scripts/: Deployment scripts
deploy.js: Hardhat script to deploy the Voting smart contract


test/: Smart contract tests
Lock.js: Example Hardhat test for a Lock contract



Smart Contract
The Voting smart contract is written in Solidity and includes the following functions:

addCandidate: Add a new candidate
vote: Cast a vote for a candidate
getAllVotesOfCandiates: Retrieve all candidates and their vote counts
getVotingStatus: Check if voting is still active
getRemainingTime: Get the remaining time for voting
voters: Check if an address has voted

The contract is deployed with a predefined list of candidates and a voting duration (in minutes).
Testing
Run tests for the smart contract using Hardhat:
npx hardhat test

Run React component tests:
npm test

Styling
The application uses CSS for styling, defined in src/App.css and src/index.css. The design is responsive and includes:

Flexbox-based layouts for centered content
Hover effects for buttons
A clean, minimalistic table for candidate data

Notes

Ensure MetaMask is connected to the correct network (e.g., localhost:8545 for Hardhat).
The contract address in constant.js must match the deployed contract.
The application assumes the Voting smart contract is deployed and accessible.

License
This project is licensed under the MIT License.
