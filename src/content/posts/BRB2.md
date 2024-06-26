---
title: BlockChain fundamentals BRB Bootcamp
published: 2024-06-22
tags: [Web3, Blogging, BRB bootcamp assignments]
category: Guides
draft: false
---
# What will be covered in this post:
- Short summary of BRB session 2
- Cryptography in Web3
- Escrow in Web3
- How Escrow Works
- Tools to Get Started in Web3

# Understanding public key cryptography & digital signatures

Public key cryptography is a foundational element in securing Web3 transactions, enabling secure, trustless exchanges on the blockchain. Here's a simplified example to illustrate how it works in the context of a Web3 transaction, such as sending cryptocurrency from one person to another:

Key Components involved in this:
- Public Key: Think of it as a mailbox address. Anyone can send mail (transactions) to this address, but only the owner with the key can open it.
- Private Key: This is the key to the mailbox. Only the owner has this key and can use it to access and send the contents (cryptocurrency) to another mailbox (public key).

Transaction Process:
- Alice Wants to Send Crypto to Bob:
    - Alice knows Bob's public key (his mailbox address).
    - Alice decides to send 1 ETH to Bob.
- Creating the Transaction:
    - Alice creates a transaction stating that she wants to send 1 ETH to Bob's public key.
    - To ensure the transaction is secure and comes from her, Alice signs the transaction with her private key. This signature proves that Alice authorized the transaction without revealing her private key.
- Broadcasting the Transaction:
    - Alice broadcasts this signed transaction to the blockchain network.
    - Miners or validators on the network verify the transaction. They use Alice's public key to confirm that the signature matches the transaction. This process ensures the transaction was not tampered with and that Alice, the owner of the private key corresponding to the public key from which the ETH is sent, authorized it.
- Transaction is Added to the Blockchain:
    - Once verified, the transaction is added to a block and appended to the blockchain.
    - Bob receives the 1 ETH. The public ledger now reflects this transfer, ensuring transparency and immutability.

Digital Signatures:
- Purpose: Digital signatures secure and verify the integrity of the transaction. They ensure that the transaction was created by the rightful owner of the funds and was not altered in transit.
- Process: The digital signature is created by encrypting the transaction's hash (a digital fingerprint) with Alice's private key. Anyone can use Alice's public key to decrypt the signature and compare it to the transaction's hash. If they match, it confirms the transaction's authenticity and integrity.

## Types of Wallets

In the session, we discussed different types of wallets used in Web3 transactions. Here are some common types:

1. **Hardware Wallets**: These are physical devices that store your private keys offline. They offer enhanced security as they are not connected to the internet, making them less vulnerable to hacking.

2. **Software Wallets**: These are applications or software programs that you can install on your computer or mobile device. They securely store your private keys and allow you to manage your cryptocurrencies.

3. **Web Wallets**: These wallets are accessed through a web browser. They are convenient to use as they don't require any installation. However, they are more susceptible to phishing attacks and hacking.

4. **Paper Wallets**: A paper wallet is a physical printout of your private and public keys. It provides an offline storage option and is considered highly secure. However, it requires careful handling to prevent loss or damage.

5. **Mobile Wallets**: These wallets are specifically designed for mobile devices. They offer convenience and allow you to manage your cryptocurrencies on the go. However, they may be less secure compared to hardware wallets.

6. **Desktop Wallets**: These wallets are installed on your desktop or laptop computer. They provide a higher level of security compared to web wallets but require regular software updates and maintenance.

It's important to choose a wallet that suits your needs and prioritize security when dealing with cryptocurrencies. Remember to research and follow best practices to protect your assets.

## Setting up a Dev Environment for Solidity

When writing Solidity code, it's important to have a suitable development environment to ensure a smooth and efficient coding experience. Here are some popular options for setting up a dev environment for Solidity:

1. **Remix IDE**: Remix is a web-based integrated development environment specifically designed for Solidity. It provides a user-friendly interface with features like code highlighting, debugging, and smart contract deployment. Remix also offers built-in Solidity compiler and Ethereum virtual machine (EVM) for testing and deploying contracts.

2. **Visual Studio Code (VS Code) with Solidity Extension**: VS Code is a widely used code editor that supports various programming languages, including Solidity. By installing the Solidity extension, you can benefit from features like syntax highlighting, code completion, and debugging. The extension also integrates with popular Solidity development tools like Truffle and Ganache.

3. **Hardhat**: Hardhat is another popular development environment for Ethereum smart contracts. It offers a wide range of features, including built-in testing, debugging, and deployment tools. Hardhat also supports TypeScript, which provides additional type safety and tooling for Solidity development.

# Escrows in Web 3 and how they work

Escrow is a financial arrangement where a third party holds and regulates the payment of funds or assets between two parties involved in a transaction. It acts as a trusted intermediary, ensuring that the funds or assets are securely held until the agreed-upon conditions are met.

In the context of Web3 and decentralized transactions, escrow plays a significant role in facilitating secure and trustless exchanges. It helps mitigate the risks associated with transacting directly between parties, especially in a decentralized and often anonymous environment.

Here's how escrow works in the context of decentralized transactions:

1. Agreement: The buyer and seller agree on the terms and conditions of the transaction, including the price, delivery, and any other relevant details.

2. Smart Contract Creation: A smart contract is created on the blockchain, which acts as the escrow agent. The smart contract includes the agreed-upon conditions and holds the funds or assets until those conditions are met.

3. Funds or Assets Deposited: The buyer deposits the funds or assets into the smart contract, which locks them until the conditions are fulfilled. This ensures that the seller will receive the payment once the conditions are satisfied.

4. Condition Verification: The smart contract verifies the fulfillment of the agreed-upon conditions. This can be done automatically through predefined rules or through an oracle that provides external data.

5. Release of Funds or Assets: Once the conditions are met, the smart contract releases the funds or assets to the seller. This ensures that the buyer's payment is only transferred when the agreed-upon conditions are satisfied.

6. Dispute Resolution: In case of any disputes, the smart contract can include predefined rules or mechanisms for resolving conflicts. This can involve arbitration, voting, or other consensus mechanisms to ensure a fair resolution.

By using escrow in Web3 transactions, participants can have increased trust and security, as the funds or assets are held in a decentralized and transparent manner. It reduces the risk of fraud, non-payment, or non-delivery, providing a more reliable and efficient way to conduct transactions in the decentralized ecosystem.

## Getting Started in Web3

To get started in Web3, you need to install and set up the following tools:
- VS Code with JS and Solidity extensions installed
- Node.js
- Hardhat (or ThirdWeb for a better experience on macOS)
- React Vite for front-end development (additional libraries required for interacting with smart contracts like Rainbow Kit or ThirdWeb)

You also need a wallet. The recommended wallet is MetaMask, but other chains may require specific wallets.

For learning resources, the r/web3 subreddit and the Superteam India Discord are great places to connect with active Web3 developer communities. You can ask questions and get support from experienced developers.

Remember to always prioritize security and research best practices when working with Web3 technologies. Happy coding!

---
