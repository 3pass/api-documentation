# 3stats API V1

## Endpoints

### /wallets

returns information about wallets

#### GET /wallets/{address}

returns information about the specified address

query parameters:

* blockHeight: type + description + example
* currentlyOwned: type + description + example

```
{
  address: '0x..',
  balances: [
    {
      chain: 'Ethereum',
      token: 'MANA',
      amount: 333
    },
    {
      chain: 'Polygon',
      token: 'MANA',
      amount: 1023
    }
  ],
  tokens: [
    {
      chain: 'Ethereum',
      contractAddress: '0xf87e31492faf9a91b02ee0deaad50d51d56d5d4d',
      contractName: 'Decentraland: LAND',
    }
  ]
}
```

TBD: what else is included in the "token" node?

#### GET /wallets/heatmaps

returns aggregated information about tokens and their holders

TBD

### /dcl

endpoints related to information about the Decentraland metaverse

#### GET /dcl/landowners

returns information about landowners in Decentraland

query parameters:

* top: type + description + example

```
[
  {
    address: '0x...',
    rankByCount: 2, // leaderboard based on total land owned
    rankByValue: 20, // leaderboard based on...?
    landsOwnedCount: 6,
    landsOwned: [
      {
        contractAddress: '0xf87e31492faf9a91b02ee0deaad50d51d56d5d4d',
        tokenId: '20416942015256307807802476445906092687221',
        owner: '0x...',
        coordinates: '59,-139',
        ...
      }
    ]
    estatesOwnedCount: 2,
    estatesOwned: [
      {
        contractAddress: '0x959e104e1a4db6317fa58f8295f586e1a978c297',
        tokenId: "4908",
        owner: '0x...',
        ...
      }
    ]
  }
]
```

#### GET /dcl/heatmaps

returns heatmap data about various data types

query parameters:

* label: type + description + example + options
* top: type + description + example

#### GET /dcl/userHistory/{address}

returns information about the specified users actions within Decentraland

TBD

#### GET /dcl/parcelHistory

returns information about the specified parcel within Decentraland

TBD

