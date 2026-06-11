# Blockchain-Based Food Donation Tracking System

A decentralized blockchain-powered food donation tracking platform built using Solidity and Ethereum Sepolia Testnet to reduce food wastage through transparent and tamper-proof donation management.

The system enables donors such as hostels, cafeterias, restaurants, and NGOs to securely publish surplus food donations, while receivers can claim and confirm pickups using Ethereum smart contracts.

---

# Project Objective

The primary goal of this project is to improve transparency, accountability, and efficiency in food donation systems using blockchain technology.

This system helps to:

* Reduce food wastage through efficient redistribution
* Maintain transparent and immutable donation records
* Prevent duplicate or fake donation claims
* Enable decentralized donation tracking without centralized control
* Improve trust between donors and receivers

---

# Team Members

### Member 1

**Name:** Fairly Sorathiya
**SRN:** PES2UG23CS189

### Member 2

**Name:** Drishti Golchha
**SRN:** PES2UG23CS185
---

# Technology Stack

| Component                  | Technology Used             |
| -------------------------- | --------------------------- |
| Smart Contract Development | Solidity                    |
| Blockchain Platform        | Ethereum                    |
| Test Network               | Ethereum Sepolia Testnet    |
| Development IDE            | Remix IDE                   |
| Wallet Integration         | MetaMask                    |
| Blockchain Interaction     | EVM-Compatible Transactions |

---

# Key Features

## 1. Create Donation

Authorized donors can publish surplus food donation details onto the blockchain.

## 2. Claim Donation

Receivers can securely claim available food donations.

## 3. Confirm Pickup

Receivers confirm successful food collection directly through smart contract execution.

## 4. Transparent Donation Tracking

All donation states including Available, Claimed, and PickedUp are permanently recorded.

## 5. Immutable Blockchain Ledger

Every transaction is stored on Ethereum Sepolia Testnet ensuring tamper-proof auditability.

## 6. Smart Contract Validation

Role-based smart contract restrictions ensure secure execution of donation workflows.

---

# Smart Contract Functions

## `createDonation()`

Used by donors to create a new food donation.

```solidity
createDonation("Burger");
```

---

## `claimDonation()`

Used by receivers to claim available donations.

```solidity
claimDonation(1);
```

---

## `confirmPickup()`

Used by receivers to confirm successful food collection.

```solidity
confirmPickup(1);
```

---

## `getDonation()`

Fetches donation details including donor, receiver, and status.

```solidity
getDonation(1);
```

---

# Workflow

## Step 1 — Donor Creates Donation

The donor creates a new donation entry.

```solidity
createDonation("Rice Packets");
```

Status becomes:

```text
Available
```

---

## Step 2 — Receiver Claims Donation

A receiver claims the available donation.

```solidity
claimDonation(1);
```

Status becomes:

```text
Claimed
```

---

## Step 3 — Receiver Confirms Pickup

The receiver confirms successful pickup.

```solidity
confirmPickup(1);
```

Status becomes:

```text
PickedUp
```

---

# Smart Contract Security

## Donor Cannot Claim Own Donation

```solidity
require(msg.sender != donor, "Donor cannot claim");
```

---

## Claimed Donations Cannot Be Claimed Again

```solidity
require(status == Status.Available, "Already claimed");
```

---

## Only Receiver Can Confirm Pickup

```solidity
require(msg.sender == receiver, "Only receiver can confirm");
```

---

# Deployment Steps

## Step 1

Open Remix IDE.

## Step 2

Paste the Solidity smart contract source code.

## Step 3

Compile using Solidity Compiler.

## Step 4

Open MetaMask and switch network to:

```text
Ethereum Sepolia Testnet
```

## Step 5

Obtain free Sepolia ETH from a faucet.

## Step 6

In Remix Environment select:

```text
Injected Provider / MetaMask
```

## Step 7

Connect MetaMask wallet.

## Step 8

Deploy the smart contract and confirm the transaction.

---

# Testing

## Test Case 1

```solidity
createDonation("Burger");
```

## Test Case 2

```solidity
claimDonation(1);
```

## Test Case 3

```solidity
confirmPickup(1);
```

## Test Case 4

```solidity
getDonation(1);
```

---

# Blockchain Details

## Blockchain Type

This project uses a:

```text
Public Blockchain
```

Specifically:

```text
Ethereum Sepolia Testnet
```

Benefits include:

* Decentralization
* Transparency
* Security
* Public verification

---

# Consensus Algorithm

Ethereum currently uses:

```text
Proof of Stake (PoS)
```

## Advantages of PoS

* Energy efficient validation
* Faster transaction confirmation
* Better scalability
* Improved decentralized security

---

# Future Improvements

* Frontend dashboard integration using React.js
* Real-time donation notifications
* QR-code based pickup verification
* NGO authentication and reputation scoring
* IPFS integration for decentralized metadata storage

---

# Conclusion

The Blockchain-Based Food Donation Tracking System demonstrates how blockchain technology can be used to create transparent, secure, and decentralized food redistribution systems.

By leveraging Ethereum smart contracts and MetaMask integration, the platform removes centralized dependency while ensuring secure and immutable donation tracking.

This project highlights practical applications of blockchain technology for solving real-world social impact problems such as food wastage and equitable food distribution.
