GhostAuth: Decentralized Identity Management (SENG 473)

GhostAuth is a decentralized identity (DID) protocol designed to solve the "central database" problem in modern authentication. By leveraging blockchain-inspired logic and client-side cryptography, it ensures that user credentials remain invisible, private, and immutable.

🚀 The Core Problem

Most websites store your password (or a hash) in a central database. If that database is hacked, every user's security is at risk. GhostAuth removes the need for a central secret store entirely.

🔐 Key Security Features

Zero-Knowledge Proof (Simulated): The application verifies that a user possesses the correct secret by matching cryptographic fingerprints (hashes). The actual secret never leaves the user's device.

Edge-Client Hashing: We use the Web Crypto API to perform SHA-256 hashing locally in the browser. The "server" or "ledger" only ever sees the final digest.

Immutable Protocol Ledger: Identities are recorded as linked blocks. Each block contains a pointer (prevHash) to the previous identity, ensuring the integrity of the entire chain.

Non-Custodial Design: Users own their identity blocks. There is no central "Reset Password" function that can be exploited by social engineering.

🛠️ Tech Stack

React.js: For the interactive, single-page protocol simulation.

Tailwind CSS: For the futuristic, high-contrast "Cyberpunk" dark-mode UI.

Lucide React: Security and blockchain-specific iconography.

Web Crypto API: Native high-speed SHA-256 implementation.

📺 Project Walkthrough Guide

For the SENG 473 YouTube submission, focus on these three phases:

Code Architecture: Open App.jsx and explain the generateHash async function. Point out that it uses the TextEncoder and subtle.digest to ensure security at the "edge" (the user's browser).

The Immutable Chain: Demonstrate the "Protocol Ledger" on the home page. Explain how blockNumber and prevHash mimic the structure of a real blockchain like Bitcoin or Ethereum.

The Proof of Concept: Register a team member, show their hash on the ledger, then log out and log back in to demonstrate that the system only grants access if the calculated hash matches the stored hash exactly.

🌐 Live Deployment

This project is optimized for deployment via GitHub Pages. Simply upload the files to a repository named GhostAuth and enable Pages in the settings to share a live, working link with your professor.

Course: SENG 473 Information Security

Team: ELYAS AMAR KHIL & SALEH AL-SHAMI

Topic: 5 - Blockchain Identity Management
