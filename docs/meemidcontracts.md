# Meem ID Smart Contracts

In order to facilitate future upgrades to Meem IDs, we use [EIP-2535 Diamonds](https://eips.ethereum.org/EIPS/eip-2535).

## Implementation

**The main proxy contract is the address you should use**. Facet addresses will change when the contract is upgraded.

## Smart Contract Quick Links

### ABI / Typescript

Full ABI with all functions: [MeemID.json](https://raw.githubusercontent.com/meemproject/meem-id-contracts/master/types/MeemID.json)

Typechain Types: [https://github.com/meemproject/meem-id-contracts/tree/master/types/ethers-contracts](https://github.com/meemproject/meem-id-contracts/tree/master/types/ethers-contracts)

### Polygon (Live Contract)

**Main Proxy Contract: [0x3D7d5f8533b19e63497e49C75ab0A045f2917F3D](https://polygonscan.com/address/0x3D7d5f8533b19e63497e49C75ab0A045f2917F3D)**

#### Facets

* AccessControlFacet: [0x7045b5f73895313DC4C0de92954e977a19c23F1b](https://polygonscan.com/address/0x7045b5f73895313DC4C0de92954e977a19c23F1b)
* MeemIdFacet: [0x01c319B678974C1722267f61dd71a07869c4031e](https://polygonscan.com/address/0x01c319B678974C1722267f61dd71a07869c4031e)
* InitDiamond: [0xC5Fc76181ac483d4167c994b63987c44d000F69c](https://polygonscan.com/address/0xC5Fc76181ac483d4167c994b63987c44d000F69c)

### Rinkeby (Testnet Contract)

**Main Proxy Contract: [0x6EC3b14B9844544c710EE48481D8A1E8130F0D7D](https://rinkeby.etherscan.io/address/0x6EC3b14B9844544c710EE48481D8A1E8130F0D7D)**

#### Facets

* AccessControlFacet: [0x6fE1b7fb300DE5376ee309960345Cd69C482Fc62](https://rinkeby.etherscan.io/address/0x6fE1b7fb300DE5376ee309960345Cd69C482Fc62)
* MeemIdFacet: [0x907657a8ec7e3b976506bA91cFb53BEDAF246557](https://rinkeby.etherscan.io/address/0x907657a8ec7e3b976506bA91cFb53BEDAF246557)
* InitDiamond: [0x4e24d27dfE37825083f92279d607ddF9d6afF3dF](https://rinkeby.etherscan.io/address/0x4e24d27dfE37825083f92279d607ddF9d6afF3dF)

## Source Code

[https://github.com/meemproject/meem-id-contracts](https://github.com/meemproject/meem-id-contracts)
