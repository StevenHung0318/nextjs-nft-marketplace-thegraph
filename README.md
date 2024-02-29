# NextJS NFT Marketplace with TheGraph

*This repo has been updated for Sepolia over Goerli.*

## 1. Git clone the contracts repo

In it's own terminal / command line, run: 

```
git clone https://github.com/StevenHung0318/hardhat-nft-marketplace
cd hardhat-nft-marketplace
yarn
```

## 2. Deploy to sepolia 

After installing dependencies, deploy your contracts to sepolia:

```
yarn hardhat deploy --network sepolia
```

## 3. Deploy your subgraph

```
cd ..
git clone https://github.com/StevenHung0318/graph-nft-marketplace
cd graph-nft-marketplace
yarn
```

Follow the instructions of the [README](https://github.com/StevenHung0318/graph-nft-marketplace/blob/main/README.md) of that repo. 

Then, make a `.env` file and place your temporary query URL into it as `NEXT_PUBLIC_SUBGRAPH_URL`.


## 4. Start your UI

Make sure that:
- In your `networkMapping.json` you have an entry for `NftMarketplace` on the sepolia network. 
- You have a `NEXT_PUBLIC_SUBGRAPH_URL` in your `.env` file. 

```
yarn dev
```

