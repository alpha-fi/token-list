# Curated Token List

This repository contains list of tokens for NEAR dapps.

Notable, the list is used for NEARswap.

## Organization

We define one list for each NEAR network. Each list is a JSON file:

+ `main-net.json`
+ `test-net.json`
+ `beta-net.json`
+ `guild-net.json`

## Structure

Each JSON file MUST be a list of object with structure:

```
name: String
symbol: String
type: Native | NEP-21 | NEP-122 | NEP-136
address: String (smart contract account address, empty if type==Native)
decimals: Number
granularity: Number | undefined (undefined if type!=NEP-136)
logoURL: String (URL)
```

Example:
```
[
    {
      "name": "NEAR",
      "symbol": "NEAR",
      "type": "Native token",
      "address": "",
      "decimals": 24,
      "logoURL": "https://raw.githubusercontent.com/trustwallet/assets/master/blockchains/near/info/logo.png"
    }, {
      "name": "GOLD",
      "symbol": "GOLD",
      "type": "NEP-21",
      "address": "gold.nearswap.testnet",
      "decimals": 24,
      "logoURL": "https://user-images.githubusercontent.com/26249903/94925431-d3f07700-04dc-11eb-8189-68fbd65e7738.png"
    }
]
```


## LICENSE

MIT. See LICENSE [file](./LICENSE)
