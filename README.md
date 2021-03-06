# Solana Dev Environment

A local Solana development environment in a container.

# Setup

Prerequisites
   * [Install NodeJS & NPM](https://nodejs.org/en/download/package-manager/)

References:
   * [Anchor Repo](https://github.com/project-serum/anchor)
   * [Anchor Docs](https://docs.rs/anchor-lang/latest/anchor_lang/index.html)
   * [Development Walkthrough](https://dev.to/dabit3/the-complete-guide-to-full-stack-solana-development-with-react-anchor-rust-and-phantom-3291)


To setup the environment run:
```bash
# Build the image
npm run image

# Pop into the dev image
npm run dev

# Create a directory to store your creds
mkdir -p /app/.devconfig

# Once you're inside of the dev image, create your wallet
solana-keygen new -o /app/.devconfig/wallet.json

# Copy the wallet over to the spot the `solana` cli expects
cp /app/.devconfig/wallet.json /root/.config/solana/id.json

# Change to localhost
solana config set --url localhost

# Runa  local Solana node
solana-test-validator
```

**Building**
* From inside the `/app/nft/` directory, run `anchor build`. This will take some time.


# Trouble shooting

**Error: AccountNotFound: pubkey=XXXXXX**

Make sure you're on the correct network (localhost)

> `solana config set --url localhost`