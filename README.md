# algokitworkshop

Welcome to your new AlgoKit project!

This is your workspace root. A `workspace` in AlgoKit is an orchestrated collection of standalone projects (backends, smart contracts, frontend apps and etc).

By default, `projects_root_path` parameter is set to `projects`. Which instructs AlgoKit CLI to create a new directory under `projects` directory when new project is instantiated via `algokit init` at the root of the workspace.

## Getting Started

To get started refer to `README.md` files in respective sub-projects in the `projects` directory.

To learn more about algokit, visit [documentation](https://github.com/algorandfoundation/algokit-cli/blob/main/docs/algokit.md).

### GitHub Codespaces

To get started execute:

1. `algokit generate devcontainer` - invoking this command from the root of this repository will create a `devcontainer.json` file with all the configuration needed to run this project in a GitHub codespace. [Run the repository inside a codespace](https://docs.github.com/en/codespaces/getting-started/quickstart) to get started.
2. `algokit init` - invoke this command inside a github codespace to launch an interactive wizard to guide you through the process of creating a new AlgoKit project

Powered by [Copier templates](https://copier.readthedocs.io/en/stable/).

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


  

---

## 📜 Smart Contract Code  
Contract Address: import { Contract , GlobalState } from '@algorandfoundation/algorand-typescript'

// A simple Dice Roller contract
export class DiceRoller extends Contract {
  // Store the last rolled dice value in global state
  lastRoll = GlobalState<number>({ key: "last_roll", initialValue: 0 })

  // Function to roll the dice
  // The caller passes in a "seed" number (like block timestamp, tx sender, etc.)
  Roll(seed: number): number {
    // Very simple pseudo-random dice roll (NOT secure randomness)
    const diceValue = (seed % 6) + 1

    // Store the result in global state
    this.lastRoll.value = diceValue

    // Return the rolled dice value
    return diceValue
  }

  // Function to get the last rolled value
  GetLastRoll(): number {
    return this.lastRoll.value
  }
}

```ts
//paste your code

