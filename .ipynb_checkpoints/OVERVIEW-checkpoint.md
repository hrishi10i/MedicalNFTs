# MedLink Project Overview

## Objective
MedLink is a decentralized platform for securely managing, sharing, and commercializing medical documents using NFTs (non-fungible tokens) on blockchain. It empowers patients and doctors with full control, security, and authenticity over health records, as well as enabling ethical sharing/selling of data to researchers and advertisers.

---

## Problem Addressed
- **Patient Inconvenience:** Fragmented and hard-to-transfer records.
- **Doctor Difficulty:** Accessing distributed or insecure data.
- **Loss of Patient Control:** Centralized data stores, privacy risks.
- **Data Quality Issues:** Researchers/advertisers often lack access to quality, ethically sourced data.

---

## Solution & Benefits
### For Patients
- **Data Security:** Records stored immutably on blockchain.
- **Authenticity:** NFTs prevent data fraud, allow provenance/tracking.
- **Full Control:** Patients decide who accesses or purchases their data.
- **Burn Feature:** Option to destroy NFT records if desired.

### For Doctors
- **Unified System:** All records accessed via NFT dashboard.
- **Blockchain Storage:** Secure, cost-effective, transparent.

---

## Technical Architecture

### 1. Smart Contract (Solidity)
- Implements ERC721-based NFT logic for medical documents.
- Main Features:
  - Minting, listing, selling, transferring, burning NFTs
  - Seller/buyer controls and record access permissions

### 2. Web Frontend (React)
- Main App routing for signup, dashboard, listing, transfer, and marketplace flows
- Integrates MetaMask or other wallets for authentication & transaction signing
- Components for patients, doctors, and business interaction

### 3. Backend/Deployment
- **Hardhat** for Ethereum dev, deployment and tests
- Deployment script generates ABI/interface for frontend
- (Metadata storage assumed via local/remote storage)

### 4. Libraries & Stack
- **Smart contract:** Solidity, OpenZeppelin, Chainlink
- **Frontend:** React, MDB React UI, Tailwind, React Router
- **Web3/Deployment:** ethers.js, Hardhat

---

## Core Workflows

1. **User Signup/Login**: Users connect a crypto wallet.
2. **Medical Record Upload**: Patients upload and mint record NFTs.
3. **NFT Marketplace**: Buy, sell, or transfer medical record NFTs.
4. **NFT Burn**: Patients may burn (destroy) their data NFT.
5. **Doctor Record Access**: Doctors view/update patient NFTs as allowed.
6. **Data Sales/Consent**: Patients can monetize their data ethically.

---

## Security & Compliance
- Enforced wallet authentication and logging
- Stated compliance with HIPAA, GDPR (privacy standards)
- Full patient access control, with revocation options

---

## How To Run
1. **Install MetaMask** (or similar wallet extension)
2. **Clone & Setup**:
    ```bash
    git clone https://github.com/Abhilash-3107/MedicalNFTs.git
    cd MedicalNFTs/
    npm install
    ```
3. **Start Frontend**:
    ```bash
    npm start
    ```
4. **Deploy Contracts (optional/dev):** Use Hardhat to deploy/update smart contracts, update frontend ABI as needed.

---

## Tech Stack Table
| Layer        | Tech         | Responsibility                    |
|--------------|--------------|-----------------------------------|
| Blockchain   | Solidity     | NFT medical record contract logic |
| Frontend     | React        | Web UI, wallet, record display    |
| Middleware   | Hardhat      | Contract deployment, ABI creation |
| Storage      | Blockchain, possibly central DB | Metadata & docs |
| Compliance   | Policy in app| HIPAA, GDPR, access control       |

---

## Further Exploration
- See `/contracts/HealthNFT.sol` for smart contract logic.
- Explore `/src/` for React components and user flows.
- Check `scripts/deploy.js` for deployment process.
- See `README.md` for basic installation info and intro.

Let us know if you need a deeper dive into any specific part!
