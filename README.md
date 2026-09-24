# ⛓️ Web3 Support & On-Chain Troubleshooting Runbook

A standardized operational reference manual designed for customer support and operations teams handling decentralized applications (dApps), non-custodial wallet integrations, and crypto transaction lifecycles.

## 🎯 Purpose
This repository serves as a proactive framework for diagnosing user friction points, resolving on-chain transaction errors, and maintaining high customer satisfaction in fast-paced Web3 environments.

---

## 📂 Runbook Index

| Module | Focus Area | Description |
| :--- | :--- | :--- |
| **[01-Wallets.md](./docs/01-Wallets.md)** | Non-Custodial Wallets | Resolving connection drops, RPC node failures, and signature requests. |
| **[02-Transactions.md](./docs/02-Transactions.md)** | On-Chain Operations | Diagnosing pending/stuck transactions, gas optimization, and TxID tracking. |
| **[03-CrossChain.md](./docs/03-CrossChain.md)** | Network & Asset Recovery | Standard protocols for handling incorrect network selections and asset routing. |

---

## 🛠️ Core Competencies Covered
* **User Advocacy:** Translating complex blockchain mechanics into clear, empathetic, non-technical instructions for retail users.
* **Risk & Security:** Identifying anomalous transaction behaviors without compromising user self-custody.
* **Escalation Protocol:** Structuring precise technical bug reports for dev teams when platform-side errors occur.

# Module 01: Non-Custodial Wallet Troubleshooting

## Common User Issues & Resolution Protocols

### 1. Wallet Connection Failures (WalletConnect / Injected Providers)
* **Symptom:** User clicks "Connect Wallet," but the modal fails to trigger, or the connection hangs indefinitely.
* **Root Cause:** Stale browser cache, conflicting browser extensions (e.g., multiple wallet extensions fighting for injection), or mobile app deep-link desynchronization.
* **Support Resolution Steps:**
  1. Advise the user to clear their browser cache and local storage for the specific dApp domain.
  2. Instruct them to disable conflicting extensions temporarily (e.g., keeping only MetaMask or Trust Wallet active).
  3. For mobile users via WalletConnect, recommend disconnecting all active sessions inside their mobile wallet app settings and re-scanning the QR code.

### 2. "User Rejected Request" / Signature Errors
* **Symptom:** Transaction or message signing fails immediately upon prompt.
* **Root Cause:** Gas estimation failure, network desync, or accidental cancellation by the user.
* **Support Resolution Steps:**
  1. Verify if the user's wallet is set to the correct network required by the smart contract.
  2. Ensure the user has sufficient native gas tokens (e.g., ETH, MATIC, BNB) to cover execution fees—not just the principal swap amount.
  3. Guide the user to manually reset their wallet account state if nonce values have desynchronized.
