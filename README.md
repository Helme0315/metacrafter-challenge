# Solana Challenge Part2 

## STEP 1

### Create SPL token
```
spl-token create-token

spl-token create-account <Token Address>

spl-token mint <Token Address> <Token Amount>
```

## STEP 2

Add created spl token address to splToken field on config.json 
Example
```
{
  "price": 5,
  "number": 10,
  "gatekeeper": null,
  "solTreasuryAccount": null,
  "splTokenAccount": null,
  "splToken": "7P71pNhqFDnGe7LNyYcDL17E7TvUiwPdk1RwmiRpiUtA",
  "goLiveDate": "2022-11-22T00:00:00Z",
  "endSettings": null,
  "whitelistMintSettings": null,
  "hiddenSettings": null,
  "storage": "nft-storage",
  "ipfsInfuraProjectId": null,
  "ipfsInfuraSecret": null,
  "awsS3Bucket": null,
  "nftStorageKey": null,
  "noRetainAuthority": false,
  "noMutable": false
}
```

### Create own NFT collection using command line
```
ts-node ./js/packages/cli/src/candy-machine-v2-cli.ts verify_assets ./js/packages/cli/assets

ts-node ./js/packages/cli/src/candy-machine-v2-cli.ts upload \
    -e devnet \
    -k ~/.config/solana/id.json \
    -cp ./js/packages/cli/config.json \
    -c metacrafters \
    ./js/packages/cli/assets

ts-node ./js/packages/cli/src/candy-machine-v2-cli.ts set_collection \
    -e devnet \
    -k ~/.config/solana/id.json \
    -c metacrafters

ts-node ./js/packages/cli/src/candy-machine-v2-cli.ts verify_upload \
    -e devnet \
    -k ~/.config/solana/id.json \
    -c metacrafters
```

## STEP 3

Download candy-machine-ui using below command line
```
git clone <Path>
```

## STEP 4

Run the UI and mint NFT.
You can check it through this repo.

## STEP 5

Send me your Solana wallet address.
Then I will send created the spl token, so you can confirm it.

Thanks!