🟦 HelloBase Mini dApp
A minimal on-chain application built on Base Mainnet, showcasing wallet connection, contract interaction, and real-time message updates.
<p align="center"> <img src="https://img.shields.io/badge/Network-Base%20Mainnet-0065FF?style=for-the-badge&logo=coinbase" /> <img src="https://img.shields.io/badge/Smart%20Contract-Verified-22c55e?style=for-the-badge&logo=ethereum" /> <img src="https://img.shields.io/badge/Frontend-HTML%2FCSS%2FJS-blue?style=for-the-badge" /> <img src="https://img.shields.io/badge/Ethers.js-v5-orange?style=for-the-badge" /> </p>
🎥 Demo (GIF)

You can upload a GIF later, then replace this placeholder.

<img src="assets/demo.gif" width="650"/>

🔗 Live dApp

👉 https://mesut006.github.io/base-mini-dapp/

📍 Smart Contract
Property	Value
Network	Base Mainnet (chainId: 8453)
Contract Address	0xD6e402b477B05f8105be4fAaC4a43E0355aCc8F8
Verified	Yes — on BaseScan
Compiler	Solidity ^0.8.x
ABI (Used by the dApp)
[
  { "inputs": [], "name": "message", "outputs": [{ "type": "string" }], "stateMutability": "view", "type": "function" },
  { "inputs": [{ "name": "newMessage", "type": "string" }], "name": "setMessage", "outputs": [], "stateMutability": "nonpayable", "type": "function" }
]

🧩 Architecture Overview
                 ┌────────────────────────┐
                 │      MetaMask UI       │
                 └───────────┬────────────┘
                             │
                             ▼
                ┌───────────────────────────┐
                │    Ethers.js (v5) Layer    │
                │ - Provider                 │
                │ - Signer                   │
                │ - Contract Instance        │
                └───────────┬───────────────┘
                             │
                             ▼
         ┌──────────────────────────────────────────┐
         │          HelloBase Smart Contract         │
         │    Base Mainnet ● Solidity 0.8.x          │
         └──────────────────────────────────────────┘

🚀 Features (Advanced)
🟦 Wallet Connection (MetaMask + Base Validation)

Prevents interaction on wrong networks

Displays chainId + user address

UI-based error handling

📡 Read On-Chain State

message() is read via a provider → no signature required.

✍️ Write On-Chain State

setMessage() triggers:

Transaction creation

User signature

On-chain execution

Automatic UI refresh

Transaction added to history list

🧾 Transaction History Panel

Fetches last 5 user interactions

Includes:

Tx Hash

Timestamp

chainId

Direct BaseScan links

🌐 GitHub Pages Deployment

Zero backend → purely client-side

Designed for full decentralization

🛠 Installation & Development

If you want to run this dApp locally:

1️⃣ Clone the repo
git clone https://github.com/Mesut006/base-mini-dapp
cd base-mini-dapp

2️⃣ Start a local HTTP server

(Needed because MetaMask rejects file:// origins)

Python method:

python -m http.server 3000


Visit:

http://localhost:3000

🧪 Local Development Notes
⚠️ MetaMask: Wrong Network Handling

The dApp checks:

if (network.chainId !== 8453) {
   showNetworkErrorBanner();
}


This prevents mis-signed transactions on the wrong chain.

⚡ Gas Optimizations

The contract is intentionally minimal:

No storage complexity

1 SSTORE on writes

0 gas on read

🔐 Security Notes

UI prevents malicious arbitrary function calls

Contract has no owner, fully public

Only the sender pays gas → no admin privileges

📂 Project Structure
base-mini-dapp/
│
├── index.html        # App UI + all JS logic
├── README.md         # Documentation
└── assets/           # (Optional) icons, screenshot, demo GIF

🌐 Social Links
Platform	URL
🐦 X (Twitter)	https://x.com/soylebisey

🐙 GitHub	https://github.com/Mesut006

✍️ Paragraph	https://paragraph.com/@0xf159092ad36e8d0524be07f703866b1866d3d94d
🧑‍💻 Author

Mesut Öztürk
Builder exploring the Base ecosystem through public experiments, on-chain applications, and open-source contributions.

⭐ Support

If you like this dApp, consider giving the repo a star ⭐
New features coming soon:

NFT-based messaging

Leaderboard

Account abstraction version

Base Paymaster integrations

📜 License

MIT License — free to use, modify, and distribute.
