# Neon Quest - A Web3 Adventure on Base Mainnet

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) Neon Quest is a blockchain-based adventure game running on the Base Mainnet. Players can connect their MetaMask wallet, initialize their character, fight monsters, search for treasure (Neon Coins), use potions, and upgrade their character's level. All player actions and character stats are stored and managed via a Smart Contract on the blockchain.

## ✨ Key Features

* **Web3 Wallet Integration:** Connects with MetaMask to interact with the Base Mainnet.
* **On-Chain Character Management:** Player stats (Score, HP, Level, Potion) are stored on the blockchain.
* **Transaction-Based Game Actions:**
    * **Initialize Player:** Start the game with initial stats.
    * **Fight Monster:** Battle to earn Neon Coins or take damage.
    * **Search Treasure:** Explore to find Neon Coins.
    * **Use Potion:** Restore HP or gain bonuses if a potion is available.
    * **Upgrade Level:** Use Neon Coins to increase character level and stats.
* **Action Log:** A history of all player actions is recorded and viewable.
* **In-Game Tutorial:** A tutorial modal to guide new players.
* **Neon-Themed User Interface:** An engaging visual design with neon effects.

## 🚀 Technologies Used

* **Frontend:** HTML, CSS, JavaScript
* **Web3 Library:** Ethers.js (v5.7.2)
* **Blockchain:** Base Mainnet (Chain ID: 8453)
* **Wallet:** MetaMask (or other `window.ethereum` compatible wallets)
* **Smart Contract:** Solidity (interaction via the included ABI)

## 🎮 How to Play

### Prerequisites

1.  **Browser with Wallet Extension:** Such as Google Chrome or Firefox with the MetaMask extension installed.
2.  **Connected to Base Mainnet:** Ensure your wallet is configured and connected to the Base Mainnet.
    * **Chain ID:** `8453` (or `0x2105` in hex)
    * **RPC URL:** `https://mainnet.base.org` or `https://rpc.base.org`
3.  **ETH on Base Mainnet:** You will need a small amount of ETH on the Base Mainnet to pay for transaction gas fees. You can obtain testnet ETH from a faucet if using a test network, or bridge ETH to Base Mainnet from another network.

### Starting Your Adventure

1.  **Open the Game:** Open the `index.html` file in your browser.
2.  **Connect Wallet:** Click the "Connect Wallet" button. Approve the connection in MetaMask and ensure you are on the Base Mainnet.
3.  **Start Game:** Once the wallet is connected, click the "Start Game" button to initialize your character on the smart contract. This may require a transaction confirmation and gas fee.
4.  **Perform Actions:**
    * **Fight Monster:** Challenge a monster to potentially earn Neon Coins.
    * **Search:** Search for treasure to acquire Neon Coins.
    * **Use Potion:** If you have a potion (`Potion: Active`), use it for positive effects.
    * **Upgrade:** Level up your character using the Neon Coins you've collected.
5.  **Monitor Stats:** Keep an eye on your Score, HP, Level, and Potion status.
6.  **View Action Log:** Check your action history in the "Action Log" section.
7.  **Tutorial:** Click the "Tutorial" button at any time for gameplay guidance.

## ⛓️ Smart Contract Details

The game interacts with a Smart Contract deployed on the Base Mainnet.

* **Network:** Base Mainnet
* **Contract Address:** `0x29a4486b8481205a24902ce4347903f14b4a0d71`
* **ABI (Application Binary Interface):** The contract ABI is included directly in the JavaScript code within the `index.html` file in the `contractABI` variable.
* **Key Contract Functions (called from the frontend):**
    * `initializePlayer()`
    * `fightMonster()`
    * `searchTreasure()`
    * `usePotion()`
    * `upgradeLevel()`
    * `getPlayerActions(address)` (view)
    * `players(address)` (view)
* **Contract Events:**
    * `ActionTaken(address player, string action, uint256 points, bool success)`
    * `PotionUsed(address player)`
    * `Upgraded(address player, uint256 newLevel)`

## 🔧 Running Locally (For Development/Testing)

1.  **Clone the Repository (if this is a repo):**
    ```bash
    git clone [YOUR_REPO_URL]
    cd [REPO_FOLDER_NAME]
    ```
2.  **Open `index.html`:** Open the `index.html` file directly in a browser that has the MetaMask extension.
    * *Note: For some Web3 functionalities or if you separate files, you might need a simple local HTTP server (e.g., using the Live Server extension in VS Code or `python -m http.server`).*
3.  Ensure your MetaMask is connected to the appropriate network (e.g., Base Mainnet for production, or a test network like Base Sepolia if you deploy a test version of the contract).
4.  If you wish to test with a different contract, modify the `contractAddress` and `contractABI` in the `index.html` file.

## 🎨 UI/UX

Neon Quest features a dark visual theme with neon color accents (primarily cyan and magenta), creating a futuristic and engaging atmosphere. `box-shadow` and `text-shadow` effects are used to enhance the neon feel. Basic responsive design is also implemented.

## 🧑‍💻 Author

* **fuero.eth**

## 📝 License

This project is licensed under the MIT License - see the `LICENSE` file (if present) for details or add license details here.
