# Web3 Vulnerabilities Lab (IDOR Demo Only)

## Overview
This lab demonstrates an Insecure Direct Object Reference (IDOR) vulnerability in a Web3 context. The application simulates a token claim endpoint that sends tokens to any wallet address without verifying ownership.

## Requirements
- Python 3.x
- Flask
- Requests

## Installation
```bash
git clone https://github.com/Mickeyax/web3-vulnerabilities-lab.git
cd web3-vulnerabilities-lab
pip install -r requirements.txt

Install dependencies:
pip install -r requirements.txt

Run the server:
python app.py

Test the vulnerabilities using an API client (e.g., Postman)
URL: http://localhost:5000/claim-airdrop

JSON body:
{
  "walletAddress": "attacker_wallet_address"
}
Fixes
SSRF: Use domain whitelisting.

IDOR: Use signed messages and role-based access control (RBAC)

References
https://www.halborn.com/blog/post/explained-the-bonqdao-hack-february-2023
https://www.quillaudits.com/case-studies/oron-wallet-security-audit
