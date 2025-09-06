# Algorand-Dice-Roll-Project

# 🎲 Dice Roller on Algorand  

Welcome to **Dice Roller**, a beginner-friendly decentralized application (dApp) built on **Algorand Smart Contracts**.  
This project is designed to help new developers understand how to build, deploy, and interact with Algorand contracts using **TypeScript**.  

---

## 📖 Project Description  

Dice Roller is a simple smart contract that simulates rolling a dice (1–6).  
It demonstrates how to:  
- Store global state in Algorand contracts  
- Write contract logic in TypeScript  
- Deploy and interact with Algorand contracts through a dApp  

---

## 💡 What it does  

1. A user calls the `Roll` function, providing a seed value.  
2. The contract calculates a dice result between **1 and 6**.  
3. The result is stored in the global state (`lastRoll`).  
4. Users can query the `GetLastRoll` function to retrieve the latest dice value.  

⚠️ **Note**: This is for **learning purposes only**. The dice logic is pseudo-random and **not cryptographically secure**.  

---

## ✨ Features  

- 🎲 **Dice Roll Simulation** – roll a dice on-chain.  
- 🌍 **Global State** – stores the latest dice result on the blockchain.  
- 📜 **TypeScript Smart Contract** – beginner-friendly code structure.  
- 🚀 **Easy to Deploy** – works with AlgoKit/Beaker toolchains.  

---

## 🔗 Deployed Smart Contract  

Contract Address: **XXX**  

---

## 📜 Smart Contract Code  

```ts
//paste your code
