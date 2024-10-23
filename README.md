Here's a revised version of the README for your **Animatica** project, reflecting the switch to the Kopli Testnet and incorporating the requested smart contract links:

---

# Animatica

## Project Overview:
![1](https://github.com/user-attachments/assets/caf5745f-52e9-449d-a428-de7887b8b9dd)

As part of our **"Digital Transformation"** initiative, we proudly introduce **Animatica**, a decentralized application (dApp) built on the **Kopli Testnet**. This project merges blockchain technology with the vibrant world of anime, creating a groundbreaking platform for **anime NFT collectible card battles**. By integrating **zk-proof technology** for enhanced privacy and trust, **Animatica** delivers a new level of engaging and strategic gameplay, where players can own, trade, and battle with their custom-made anime character NFTs in a fully decentralized environment.

### Contract Addresses:
- **Main Contract 1**: [0xea823440cdfd8a97fcf90a9c14d04096a1a721c0](https://kopli.reactscan.net/rvms/0xea823440cdfd8a97fcf90a9c14d04096a1a721c0)
- **Main Contract 2**: [0xc7203561EF179333005a9b81215092413aB86aE9](https://kopli.reactscan.net/rvms/0xc7203561EF179333005a9b81215092413aB86aE9)

```
require("@nomiclabs/hardhat-waffle");
require("@nomiclabs/hardhat-ethers");
require('dotenv').config();
const fs = require('fs');

task("accounts", "Prints the list of accounts", async (taskArgs, hre) => {
  const accounts = await hre.ethers.getSigners();

  for (const account of accounts) {
    console.log(account.address);
  }
});

module.exports = {
  defaultNetwork: "hardhat",
  networks: {
    hardhat: {
      chainId: 1337
    },
    localhost: {
      url: "http://127.0.0.1:8545"
    },
    kopli: {
      url: "https://kopli-rpc.rkt.ink",
      accounts: [process.env.privateKey],
      chainId: 5318008,
    }
  },
  solidity: {
    version: "0.8.4",
    settings: {
      optimizer: {
        enabled: true,
        runs: 200
      }
    }
  }
};

```

<br></br>
![h1](https://github.com/user-attachments/assets/3f64e4df-3e44-4ec1-8b15-3740983fe3d0)

### Vision:
Imagine the thrill of card games: battling, trading, and collecting, where each card boasts unique stats like **"Attack," "Defense," "Speed,"** and **"Health."** Our vision is to bring that excitement to the blockchain with **Animatica**, a decentralized platform where anime enthusiasts can upload their own **anime-themed character cards** and engage in competitive battles.

Built on the **Kopli Testnet**, **Animatica** offers **fast, low-cost, scalable gameplay**, ensuring seamless blockchain interactions. Players will enjoy full ownership of their assets, with every move and trade recorded transparently and securely on the blockchain.

### Why Kopli and Blockchain?
We selected **Kopli Testnet** as the core technology because it offers everything a blockchain-based game requires:

- **Fast Transactions**: Kopli ensures that trades, battles, and card uploads happen almost instantly, enhancing the gaming experience.
- **Low Fees**: Affordable transaction fees let players focus on the fun without worrying about high costs.
- **Decentralization**: Kopli guarantees a decentralized experience where players fully control their assets, free from central authorities.
- **Cross-Chain Compatibility**: The platform enables smooth interactions across different blockchains, supporting seamless cross-chain transactions.

### Key Features:

#### 1. **zk-Proof Technology** (Zero-Knowledge Proofs):
**Animatica** integrates **zk-proof** technology to maintain **player privacy** while ensuring the validity of every battle and trade. This allows players to engage in the game without revealing sensitive details, creating an elevated, trustless environment where moves are proven without compromising security.

#### 2. **Kopli Testnet**:
Building on the **Kopli Testnet** provides **Animatica** with lightning-fast, low-cost transactions that power a **decentralized gaming ecosystem**. Players can trade, battle, and collect anime NFTs without the limitations often seen in other blockchains.

#### 3. **Fluid Protocol Integration**:
To ensure **cross-chain scalability**, **Animatica** incorporates **Fluid Protocol** to enable **fluid** and seamless transactions across different networks. This feature is essential for building a scalable platform that interacts smoothly with other blockchain ecosystems.

### Tech Stack:

- **Solidity** for writing smart contracts
- **ReactJS** and **NextJS** for frontend development
- **Hardhat** for blockchain testing and development
- **Tailwind CSS** for crafting a stunning, responsive user interface
- **IPFS** for decentralized storage of anime character card uploads
- **Kopli Testnet** as the main blockchain to drive the dApp
![image](https://dev.reactive.network/assets/images/global-processing-flow-c8acdaeb0cd80f98a4f753ff5fccc1ee.png)
![arch](https://github.com/user-attachments/assets/b0933238-c058-4200-98e5-f464200f4758)

### What the dApp Does:
**Animatica** provides a decentralized marketplace and gaming arena for **anime-themed collectible card battles**. Users upload custom character cards through **IPFS**, creating NFTs (ERC721 tokens) that they can trade, sell, or use in battles. Players compete based on their character’s stats like **Attack**, **Defense**, **Speed**, and **Health**, and every game action is logged transparently on the blockchain, ensuring **fairness and trustless interactions**.

Additionally, a **bidding system** for rare and powerful anime character cards adds a competitive twist. **zk-proof technology** ensures that trades and battles are done with **maximum privacy**, without revealing confidential details.
![2](https://github.com/user-attachments/assets/7f2f7f2e-07f7-4d0c-aa81-ba73c941d9b8)

### How We Built It:
We designed **Animatica** with the user in mind, using **Kopli**'s powerful blockchain features to create an **intuitive, scalable, and secure dApp**. We used **ERC721** standards for NFTs, integrated **zk-proof** technology for privacy, and leveraged **Fluid Protocol** to enable cross-chain operations. **IPFS** provides decentralized storage for custom card uploads, ensuring that the platform remains fully decentralized and user-friendly.

### Challenges We Faced:
- Integrating **zk-proofs** to balance privacy with performance.
- Solving cross-chain compatibility issues between different blockchains.
- Optimizing gas fees and debugging smart contracts on the **Kopli Testnet**.
- Time management challenges during development and feature integration.

### Accomplishments We’re Proud Of:
We’re proud of creating a fully decentralized anime-themed card battle platform that successfully integrates **zk-proofs** and **Fluid Protocol**. Our platform allows users to truly **own, trade, and battle** with anime NFTs, delivering both **fun and security** within the blockchain ecosystem.

### What We Learned:
This project deepened our understanding of **zk-proof** technology and its applications in preserving user privacy. We also learned about the intricacies of **cross-chain transactions**, and how to create a seamless, scalable gaming platform on **Kopli**.

### What’s Next:
Next, we aim to enhance the platform with more advanced **zk-proof** privacy measures and add exciting new features like **tournaments, rewards, and rare card drops**. Expanding **cross-chain support** will also be a key focus, allowing **Animatica** to scale and interact with other blockchain ecosystems.

---

**Animatica** is more than just a game—it’s a revolutionary platform where anime fans and blockchain enthusiasts can immerse themselves in a world of **collectible card battles**. Join us on the **Kopli Testnet** and experience the future of decentralized anime gaming. Fully **own, trade, and compete** with your favorite anime characters, and become a part of the next big thing in blockchain-based gaming!

Images:
![h4](https://github.com/user-attachments/assets/cd972d87-4056-4958-a089-24f60952a91b)

![h2-3](https://github.com/user-attachments/assets/9d5a48f7-31bd-4347-9525-20ba3b97fb5d)
![h3](https://github.com/user-attachments/assets/53c36746-b87b-45bb-82fd-eafe7071f366)
![h2-2](https://github.com/user-attachments/assets/1ae64ab4-3023-488d-a1d1-d5416de3beac)
![h2-1](https://github.com/user-attachments/assets/5933ad28-09ec-4ff6-bd32-cd3d74f60478)
![h5](https://github.com/user-attachments/assets/11ae9d1e-9c0b-4627-8df1-6001d2d6b7b7)
![h6](https://github.com/user-attachments/assets/7acc5d31-c9fe-499b-97f4-0a723a8b9b15)
