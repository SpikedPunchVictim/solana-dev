# Solana Dev Environment

A local Solana development environment in a container.

# Setup

Prerequisites
   * [Install NodeJS & NPM](https://nodejs.org/en/download/package-manager/)


To setup the environment run:
```bash
# Build the image
npm run image

# Pop into the dev image
npm run dev

# Once you're inside of the dev image, create your wallet
solana-keygen new -o /app/.devconfig/wallet.json
cp /app/.devconfig/wallet.json /root/.config/solana/id.json


```