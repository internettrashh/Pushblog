---
title: Understanding Web 3 Fundamentals
published: 2022-07-01
tags: [Web3, Blogging,BRB bootcamp assignments]
category: Guides
draft: false
---
## what are we going to Discuss in this blog
- short intro to web 3
- intro to Blockchin tech
- consus mechanism
- intro to smart contracts
- scaling  blockchains
- web 3 applications

# short intro to web3

## what exactly is web 3?
 Before we  discuss this we need to fist understand what is web 1.0 and web2.0 
 ### THE STATIC WEB
 in the 90s all websites were static and read only , there was rareley any user intput to websites basically Web 1.0 is like the first version of the internet, where most things were just for looking at, kind of like reading a book or looking at a poster. You couldn't really talk back to it or interact much. Websites were simple, mostly text and some pictures, and you couldn't do things like post your own videos, make comments, or like and share stuff. It was more about just getting information from the internet, not really about talking or sharing with others online.


what is web2.0??
### THE INTERACTIVE WEB

Web 2.0 is like the second version of the internet where things became more interactive and social. Imagine if your book could let you write on its pages, share your thoughts with friends, and even let them write back. That's what Web 2.0 did for the internet. It allowed people to not just read content, but also create their own, like posting photos, making comments, and sharing things with others. Websites became more like apps, where you could do things rather than just look at things. It's all about being able to interact, participate, and collaborate online.

now what is web 3.0??
### THE DECENTRALIZED WEB

Web 3.0 is like the third version of the internet, where it's not just interactive but also smart and decentralized. Imagine if the internet was a big city. In Web 1.0, you could only look at the buildings from the outside. In Web 2.0, you could go inside the buildings, talk to people, and interact with things. Now, in Web 3.0, it's like everyone can help build or change the buildings, own a piece of them, and even have a say in how the city is run, without needing a central mayor or company controlling everything.

It uses technology like blockchain, which is a way to keep records that everyone can trust without needing a central authority. This makes things like digital money (cryptocurrencies), smart contracts (agreements that run automatically when conditions are met), and decentralized apps (apps that run on a network of computers instead of just one server) possible. It's all about giving power back to the users and creators, making the internet more open, secure, and without needing to trust or rely on big companies as much.


## WHAT IS THE BLOCKCHAIN???
Blockchain is like a digital ledger or notebook that everyone can see and use, but no one can erase or change what's already written in it. Imagine you and your friends have a notebook where you keep track of who borrowed what video game from whom. Every time someone borrows or returns a game, you write it down in the notebook. Now, imagine this notebook is magical: once you write something, it can't be erased or changed, and everyone has a copy of it, so everyone always knows who has what game.

In the digital world, blockchain works similarly. It keeps track of transactions (like sending digital money, or cryptocurrencies, from one person to another) in "blocks" of information. Each block is connected to the one before and after it in a "chain," creating a complete history that can't be altered. This makes it very secure because to change any information, you'd have to change it in every copy of the ledger, which is practically impossible because the ledger is distributed across many computers around the world.

Blockchain is the technology behind cryptocurrencies like Bitcoin, but it can also be used for other things, like making sure digital contracts are automatically fulfilled or proving ownership of digital items without needing a central authority like a bank or government. It's all about creating trust in a digital space where everyone can agree on what's true without needing a middleman.

(THESE BLOCKCHAIN RECORDS CAN BE VISUALIZED ON WEBSITES LIKE ETHERSCAN , WHILE BUILDING WEB 3 APPS WE CAN READ THE BLOCKCHAIN BY USING SOMETHING CALLED RPCs)

## UNDERSTANDING SOME BUZZWORDS RELATED TO BLOCKCHAIN AND WEB3

- CONSENSUS ALGORITHM
 In the digital world of blockchains, a consensus mechanism is a set of rules that helps all the computers in the network agree on the same information or decision, even if they don't know or trust each other. Since blockchain is like a shared notebook that everyone can write in, it's important that everyone agrees on what gets written to prevent cheating or mistakes.

 There are different ways (mechanisms) to reach this agreement. One popular method is called "Proof of Work," where computers solve complex puzzles to prove they've done some work to earn the right to add new information to the blockchain. Another method is "Proof of Stake," where the right to add new information is based on how much digital currency you're willing to "lock up" or stake as a form of security.

These mechanisms make sure that everyone plays by the rules, creating a trustworthy and secure system where everyone agrees on what's true, without needing a central authority to decide. It's like having a fair and transparent way for your class to decide on the field trip destination, where every vote counts.


- Transaction Fee in Crypto
Imagine you want to send a letter to a friend in another city, and you pay the post office to deliver it for you. In the crypto world, when you want to send cryptocurrency to someone, you pay a small fee for the network (like the post office) to process and confirm your transaction. This fee is called a transaction fee.

- Miners & Validators
Miners and validators are like the workers in the post office who sort and deliver your mail. In the crypto world, miners use their computers to solve complex puzzles to confirm transactions and add them to the blockchain. Validators do a similar job but in a different way, often by checking and agreeing on transactions without the complex puzzles, depending on the blockchain's rules.

- Block Rewards
When miners or validators successfully add a block of transactions to the blockchain, they get a reward, known as a block reward. It's like getting a tip for delivering a lot of mail correctly and on time. This reward usually comes in the form of the blockchain's own cryptocurrency.

- Fungible Tokens
Fungible tokens are like regular coins or banknotes. Each one is exactly the same as another of the same value. For example, one Bitcoin is always equal to another Bitcoin, just like one dollar is always equal to another dollar.

- Non-Fungible Tokens (NFTs)
Non-fungible tokens are more like collectible items, such as a unique baseball card or a one-of-a-kind painting. Each NFT is unique and can't be replaced by another NFT, even if they're part of the same collection. They're used to prove ownership of digital items like artwork, music, or videos on the blockchain.



# Introductions to smart Contracts

Smart contracts are like automatic vending machines for agreements and transactions. Imagine you and a friend agree that if you do a certain task, your friend will give you some candy. Instead of trusting your friend to give you the candy after you've done the task, you both use a special vending machine. You do the task, and the machine automatically gives you the candy, no need for your friend to remember or be there to give it to you.

In the digital world, smart contracts work on the blockchain. They are like self-executing contracts with the terms of the agreement directly written into lines of code. The code and the agreements contained therein exist across a distributed, decentralized blockchain network. Smart contracts automatically enforce and execute the terms of the agreement when the conditions are met, without needing a middleman.

For example, if you're buying a digital artwork, the smart contract might say that once you pay the agreed amount of cryptocurrency, the digital artwork's ownership automatically transfers to you. Everything happens automatically and transparently, ensuring that everyone involved does what they agreed to do.

heres what a simple smart contract for a crypto token looks like :
(yes right you put all your money into somethin that was built using a few lines of code )
````solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleToken {
    // Mapping to keep track of token balances
    mapping(address => uint256) public balanceOf;

    // Event that logs the minting of tokens
    event Mint(address indexed to, uint256 amount);

    // Constructor function to set initial balances
    constructor() {
        // Initially mint some tokens to the contract creator
        mint(msg.sender, 1000);
    }

    // Function to mint tokens
    function mint(address _to, uint256 _amount) public {
        // Increase the balance of '_to' address by '_amount'
        balanceOf[_to] += _amount;
        // Emit an event for the minting action
        emit Mint(_to, _amount);
    }
}
````

# What is block chain scaling ??

Blockchain scaling is like trying to make a narrow road wider so more cars can travel on it at the same time without getting stuck in traffic. Originally, blockchains (like Bitcoin and Ethereum) were like narrow roads where only a few transactions could pass at a time. As more people started using them, the "road" got crowded, leading to slow transaction times and higher fees for getting transactions processed.

To solve this, various methods are being developed to "widen the road" or even build additional roads. Here are a few ways this is being done:

Layer 1 Scaling: This is like making the original road wider. It involves changes to the blockchain itself to increase its capacity. Examples include increasing the size of blocks (so each block can hold more transactions) or improving the blockchain's protocol to process transactions more efficiently.

Layer 2 Scaling: This is like building additional roads that connect to the main road. These are separate networks or technologies that sit on top of the existing blockchain and handle transactions separately. Later, they settle the final state of these transactions back on the main blockchain. It helps in handling more transactions without clogging the main network. Examples include Lightning Network for Bitcoin and various scaling solutions for Ethereum like rollups.

Sharding: Imagine breaking the road into several smaller paths, where each path is used by a different group of cars. In blockchain, sharding splits the network into smaller pieces (shards) that can process transactions in parallel, significantly increasing the network's capacity.

By implementing these and other scaling solutions, blockchains aim to handle more transactions quickly and at lower costs, making them more practical for everyday use and capable of supporting a larger number of users and applications.


# what is tokenomics:
Tokenomics refers to the economics of a cryptocurrency or token, encompassing all the factors that contribute to its value, demand, supply, and long-term viability. It's like the rulebook for a game, outlining how players can earn, spend, and trade the game's currency, which in this case, is the token. Here are some key terms and concepts involved in tokenomics:

- Supply & Demand: The total supply of tokens and how they are distributed can greatly affect their value. Some tokens have a fixed supply, creating scarcity, while others have mechanisms to increase or decrease supply based on certain conditions.

- Distribution: How tokens are initially distributed to users, such as through sales, airdrops, or as rewards, can impact who controls the majority of the tokens and how they are used within the ecosystem.

- Utility: This refers to what you can do with the token. For example, it might give you voting rights within the project, pay for services, or be staked to earn rewards. The more utility a token has, the more demand there might be.

- Incentives: These are rewards for participating in the network, such as earning tokens for validating transactions or providing liquidity. Incentives help secure the network and encourage user participation.

- Burn Mechanisms: Some projects "burn" or permanently remove a portion of tokens from circulation, usually to reduce supply and potentially increase value.

- Governance: In decentralized projects, token holders often have the right to vote on decisions affecting the project's future. The way governance rights are distributed among token holders can significantly influence the project's direction.

- Staking: Many projects allow token holders to "stake" their tokens as a way to participate in network security and governance, often earning rewards in return.

- Vesting Periods: To prevent early investors from selling all their tokens immediately after a project launches, which could drastically reduce the token's price, tokens are often subject to vesting periods during which they cannot be sold.

Understanding tokenomics is crucial for anyone looking to invest in or use cryptocurrencies, as it helps to assess the potential risks and rewards associated with a token.

# Some major Applications and invations in web 3

## Dapps
DApps, or decentralized applications, are applications that run on a blockchain or decentralized network, ensuring they operate without being controlled by a single authority. Unlike traditional apps, which run on centralized servers, DApps connect users and providers directly, without the need for intermediaries. This setup enhances transparency, security, and integrity, as the data and operations are distributed across multiple nodes in the network.

Key characteristics of DApps include:

- Decentralization: They are not controlled by a single entity. Their backend code (smart contracts) runs on a decentralized network, not a centralized server.

- Open Source: Ideally, DApps are open source, meaning their code is available for scrutiny and contributions, ensuring transparency and community trust.
Incentivization: Users and network participants are often rewarded with tokens or digital assets for their contributions, such as securing the network, validating transactions, or providing development efforts.

- Protocol/Algorithm: DApps operate on a consensus mechanism, such as Proof of Work (PoW) or Proof of Stake (PoS), which helps in validating transactions and maintaining the integrity of the decentralized network.

DApps can span various domains, including finance (DeFi), gaming, social media, and more, leveraging the blockchain's benefits to offer services that are less prone to censorship, downtime, and data breaches.

## DAOs
DAOs, or Decentralized Autonomous Organizations, are organizations represented by rules encoded as a computer program that is transparent, controlled by the organization members and not influenced by a central government. DAOs are the most effective way of establishing a digital company and are efficient for managing a common fund without the need for traditional management structures.

Here are key features of DAOs:

Decentralized Governance: DAOs operate on a blockchain, allowing decisions to be made by consensus among its members rather than a central authority. Voting rights are often tied to token ownership, with proposals and decisions made through a transparent voting process.

Smart Contracts: The rules of the organization are embedded into smart contracts on the blockchain. These contracts execute automatically based on the code's instructions, ensuring that the organization's rules are followed without human intervention.

Token-based Incentives: Members or stakeholders in a DAO often hold tokens that represent voting power. The more tokens a member holds, the greater their ability to influence decisions. Tokens can also incentivize activities that contribute to the DAO's goals.

Transparency and Security: Since DAOs are built on blockchain technology, all transactions and rules are recorded on a public ledger, ensuring transparency. This setup also provides security and resistance to tampering.

Autonomy: Once deployed on the blockchain, DAOs can operate without human intervention, guided by the pre-written rules in the smart contracts.

DAOs can be used for a variety of purposes, including venture capital funds, charitable organizations, decentralized investment funds, or even to govern a decentralized application (DApp). They represent a new form of organizational structure that is open, transparent, and democratic.

---
