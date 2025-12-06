🟦 HelloBase Mini dApp

A simple, clean, and fully functional on-chain mini application built on Base by Mesut Öztürk.

This dApp allows users to connect their wallet, read a message stored in a verified smart contract, and update it directly on-chain.
It’s a perfect starter project for developers entering the Base ecosystem.

🚀 Features

🔗 Connect wallet via MetaMask

📡 Interact with a verified smart contract on Base

📝 Read the stored message()

✍️ Update the message using setMessage()

🧾 Transaction history panel (last 5 txs)

🌐 Fully hosted on GitHub Pages

💙 Base-themed UI & clean UX

🧠 Technologies Used
Tech	Purpose
Solidity (0.8.x)	Smart contract
Ethers.js v5	Wallet connection & contract interactions
MetaMask	Provider & signing
HTML / CSS / JavaScript	Frontend
GitHub Pages	Deployment
Base Mainnet	Contract network
🔧 Smart Contract

Contract Address:

0xD6e402b477B05f8105be4fAaC4a43E0355aCc8F8


The contract exposes two simple functions:

function message() public view returns (string memory);
function setMessage(string memory newMessage) public;


The contract is verified on BaseScan.

🌐 Live Demo

👉 https://mesut006.github.io/base-mini-dapp/

📸 Screenshot

(Optional — you can upload one as screenshot.png and it will appear here.)

<img src="https://raw.githubusercontent.com/Mesut006/base-mini-dapp/main/screenshot.png" width="650"/>

🧭 How It Works

Connect wallet
The dApp requests connection via MetaMask and ensures you're on the Base network.

Read current message
Calls the message() view function and displays the stored on-chain value.

Write new message
Sends a transaction to setMessage().
Once confirmed, the UI updates automatically.

Transaction History
Shows the last 5 interactions with direct BaseScan links.

📂 Project Structure
base-mini-dapp/
│
├── index.html     # Main frontend file
├── README.md      # Project documentation
└── assets/        # Optional images/icons

💙 Social Links

🐦 X (Twitter): https://x.com/soylebisey

🐙 GitHub: https://github.com/Mesut006

✍️ Paragraph: https://paragraph.com/@0xf159092ad36e8d0524be07f703866b1866d3d94d

⭐ Support the Project

If you like this mini dApp, consider starring the repository! ⭐
More Base features are coming soon: tokens, NFTs, leaderboards, and deeper smart contract interactions.

🛠 Developer

Mesut Öztürk
A builder exploring the Base ecosystem with clean code, public on-chain experiments, and community-focused projects.

📜 License

MIT License — free to use, modify, and build upon.
