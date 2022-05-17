# Decentraland Api

## Stats

Get global stats about Decentraland


**Result**
```
{"ok": true, 
"data":[ 
"uniqueUsers":....,
"newUsers":....,
"transactions":...,
"topCountries":[....],
...
]}
```

## Landowners

Get the biggest landowners, sorted.

Options:
- sortKey: either `total`, `estates`, `parcels` or `walletValue`. 
See [wallets](../wallets/wallets.md) for more informations.
- blockHeight: The ethereum block at which the query should stop, default `latest`

**Example**:
`/v1/dcl/landowners?sortKey=total`
**Result**:
```
{"ok": true, 
"data":[ 
{"address":"0x1463b7162103247c5d464f104f7c9da61dea1bfc","total":3340,"parcels":2919,"estates":18,"walletValue":399393},
{"address":"0x0ba6a24246ab3cfc9d843373d76d8fd7fd7a3430","total":1790,"parcels":983,"estates":20,"walletValue":91287373},
{"address":"0x5326a48a8badfbbf2fb6c4a03ae6685919e3040f","total":1652,"parcels":18,"estates":12,"walletValue":9789},
...
]}
```


## Users

Get highest value users

Options:
- sortKey: either `walletValue`, `timeSpent`
- labels: limit the query to some types of users labels, like `whale`, `new`, `bot`, ...
- blockHeight: The ethereum block at which the query should stop, default `latest`

**Example**:
`/v1/dcl/users?sortKey=total&labels=whale`
**Result**:
```
{"ok": true, 
"data":[ 

...
]}
```

## User

Info about a user

Options:

**Example**:
`/v1/dcl/user/address`
**Result**:
```
{"ok": true, 
"data":[ 

...
]}
```
## Parcels

List of parcels, sorted.


## Parcel

Info about a parcel

**Result**:
```
{"ok": true, 
"data":[ 
"visitors":[....],
"transactions":[....],
...
]}
```
