# Meem ID Smart Contracts

In order to facilitate future upgrades to Meem IDs, we use [EIP-2535 Diamonds](https://eips.ethereum.org/EIPS/eip-2535).

## Implementation

**The main proxy contract is the address you should use**. Facet addresses will change when the contract is upgraded.

## Smart Contract Quick Links

### ABI / Typescript

Full ABI with all functions: [MeemID.json](https://raw.githubusercontent.com/meemproject/meem-id-contracts/master/types/MeemID.json)

Typechain Types: [https://github.com/meemproject/meem-id-contracts/tree/master/types/ethers-contracts](https://github.com/meemproject/meem-id-contracts/tree/master/types/ethers-contracts)

### Polygon (Live Contract)

Coming Soon...

**Main Proxy Contract: [0xb3a3cE42A26a2feFc4FCcE8400700C7059Fe0e2F](https://polygonscan.com/address/0xb3a3cE42A26a2feFc4FCcE8400700C7059Fe0e2F)**

#### Facets

* AccessControlFacet: [0xa3a11c54b941eDA3892b1307e2f7ca962e16612f](https://polygonscan.com/address/0xa3a11c54b941eDA3892b1307e2f7ca962e16612f)
* MeemIdFacet: [0x07016DFc6B401d577Bd37de6F42aDb04459b782d](https://polygonscan.com/address/0x07016DFc6B401d577Bd37de6F42aDb04459b782d)
* InitDiamond: [0x6c13e56D554A4a683699e71cc8EAD37D9A70749b](https://polygonscan.com/address/0x6c13e56D554A4a683699e71cc8EAD37D9A70749b)

### Rinkeby (Testnet Contract)

**Main Proxy Contract: [0x6EC3b14B9844544c710EE48481D8A1E8130F0D7D](https://rinkeby.etherscan.io/address/0x6EC3b14B9844544c710EE48481D8A1E8130F0D7D)**

#### Facets

* AccessControlFacet: [0x6fE1b7fb300DE5376ee309960345Cd69C482Fc62](https://rinkeby.etherscan.io/address/0x6fE1b7fb300DE5376ee309960345Cd69C482Fc62)
* MeemIdFacet: [0xF46f4cd9f2c7f2d3a70502f8C5c43Bd63cb9a5d3](https://rinkeby.etherscan.io/address/0xF46f4cd9f2c7f2d3a70502f8C5c43Bd63cb9a5d3)
* InitDiamond: [0x4e24d27dfE37825083f92279d607ddF9d6afF3dF](https://rinkeby.etherscan.io/address/0x4e24d27dfE37825083f92279d607ddF9d6afF3dF)

## Source Code

[https://github.com/meemproject/meem-id-contracts](https://github.com/meemproject/meem-id-contracts)
