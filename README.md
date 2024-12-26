# Foundry Lottery

Welcome to the **Foundry Lottery** project! This repository contains a decentralized lottery application built on Ethereum using Foundry, a fast and modern toolchain for Ethereum smart contract development.

---

## 🚀 Project Overview

The Foundry Lottery project is a decentralized application (dApp) where users can participate in a lottery by submitting entries via a smart contract. The winner is selected randomly, ensuring fairness and transparency through blockchain technology.

Key features of the project:

- **Random Winner Selection**: Ensures fairness using verifiable randomness.
- **Decentralized Execution**: All interactions occur on-chain, making the lottery trustless.
- **Secure and Transparent**: Leveraging Ethereum's immutability and smart contract technology.

---

## 📂 Project Structure

```
Foundry_Lottery
├── contracts/       # Solidity smart contracts
├── scripts/         # Deployment and interaction scripts
├── test/            # Testing scripts using Foundry
├── lib/             # External libraries
├── forge.toml       # Foundry configuration file
├── README.md        # Project documentation
└── .gitignore       # Git ignore rules
```

---

## ⚙️ Prerequisites

Before running or contributing to this project, ensure you have the following installed:

- [Node.js](https://nodejs.org/) and npm
- [Foundry](https://book.getfoundry.sh/)
- [Git](https://git-scm.com/)

---

## 🛠️ Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Nachiketh1704/Foundry_Lottery.git
   cd Foundry_Lottery
   ```

2. Install Foundry dependencies:

   ```bash
   forge install
   ```

3. Install Node.js dependencies (if applicable):

   ```bash
   npm install
   ```

Alternatively, use the provided `Makefile` commands:

- To install dependencies:

   ```bash
   make install
   ```

- To clean the project:

   ```bash
   make clean
   ```

---

## 🚀 Usage

### 1. Deploy the Smart Contract

Use Foundry to deploy the lottery contract:

```bash
forge script scripts/DeployLottery.s.sol --rpc-url <YOUR_RPC_URL> --private-key <YOUR_PRIVATE_KEY> --broadcast
```

Alternatively, use the Makefile:

```bash
make deploy RPC_URL=<YOUR_RPC_URL> PRIVATE_KEY=<YOUR_PRIVATE_KEY>
```

### 2. Interact with the Lottery

Once deployed, you can interact with the smart contract using scripts in the `scripts/` directory or via the Ethereum blockchain explorer for your network.

#### Enter the Lottery:

Call the `enterLottery` function with the required entry fee:

```bash
forge script scripts/EnterLottery.s.sol --rpc-url <YOUR_RPC_URL> --private-key <YOUR_PRIVATE_KEY> --broadcast
```

Alternatively, use the Makefile:

```bash
make enter RPC_URL=<YOUR_RPC_URL> PRIVATE_KEY=<YOUR_PRIVATE_KEY>
```

#### Pick a Winner:

Call the `pickWinner` function to randomly select and reward the winner:

```bash
forge script scripts/PickWinner.s.sol --rpc-url <YOUR_RPC_URL> --private-key <YOUR_PRIVATE_KEY> --broadcast
```

Alternatively, use the Makefile:

```bash
make pick_winner RPC_URL=<YOUR_RPC_URL> PRIVATE_KEY=<YOUR_PRIVATE_KEY>
```

---

## 🔧 Configuration

### Foundry Configuration

The `forge.toml` file contains the configuration for Foundry. Update the RPC URL and private key as per your requirements:

```toml
[rpc]
default = "<YOUR_RPC_URL>"

[etherscan]
key = "<YOUR_ETHERSCAN_API_KEY>"
```

---

## 🧪 Testing

Foundry's testing suite is used to ensure the correctness of the contracts.

Run all tests:

```bash
forge test
```

Alternatively, use the Makefile:

```bash
make test
```

View test coverage:

```bash
forge coverage
```

---

## 📖 Documentation

The smart contracts are documented inline for better understanding. For a detailed explanation of each function, refer to the comments in the `contracts/` directory.

---

## 🌟 Features

- **Decentralized and Transparent**: Entire lottery process runs on Ethereum.
- **Randomized Winner Selection**: Uses Chainlink VRF or equivalent randomness for fairness.
- **Extensible Architecture**: Modular design for future enhancements.

---

## 🤝 Contributing

Contributions are welcome! Follow these steps to contribute:

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add your feature"
   ```

4. Push to the branch:

   ```bash
   git push origin feature/your-feature
   ```

5. Create a pull request.

---

## 🛡️ License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## 📬 Contact

For questions or feedback, reach out to:

- GitHub: [Nachiketh1704](https://github.com/Nachiketh1704)

---

## 🙌 Acknowledgements

- [Foundry](https://book.getfoundry.sh/) for the powerful Ethereum development tools.
- [Ethereum](https://ethereum.org/) for the decentralized platform.
- [Cyfrin](https://cyfrin.io/) for their excellent educational resources.
- [Updraft](https://github.com/PatrickAlphaC/updraft) for inspiring and guiding aspects of this project.
- Open-source community for continuous inspiration and guidance.