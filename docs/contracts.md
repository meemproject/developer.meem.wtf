# Smart Contracts

In order to facilitate future upgrades to Meems, we use [EIP-2535 Diamonds](https://eips.ethereum.org/EIPS/eip-2535).

## Implementation

**The main proxy contract is the address you should use**. Facet addresses will change when the contract is upgraded.

## Smart Contract Quick Links

### ABI / Typescript

Full ABI with all functions: [Meem.json](https://raw.githubusercontent.com/meemproject/meem-contracts/master/types/Meem.json)

Typechain Types: [https://github.com/meemproject/meem-contracts/tree/master/types/ethers-contracts](https://github.com/meemproject/meem-contracts/tree/master/types/ethers-contracts)

### Polygon

**Coming Soon**

### Rinkeby Testnet

**Main Proxy Contract: [0x87e5882fa0ea7e391b7e31E8b23a8a38F35C84Ac](https://rinkeby.etherscan.io/address/0x87e5882fa0ea7e391b7e31E8b23a8a38F35C84Ac)**

#### Facets

* AccessControlFacet: [0x1fE8d8A48181F99EeEAbF5b580e05D42699E517f](https://rinkeby.etherscan.io/address/0x1fE8d8A48181F99EeEAbF5b580e05D42699E517f)
* ERC721Facet: [0x6fF4a58A037dB94B5F402A19C335C729461040b3](https://rinkeby.etherscan.io/address/0x6fF4a58A037dB94B5F402A19C335C729461040b3)
* InitDiamond: [0x8268529c16727cf9a6eF2Ec3f5964A6246752d5f](https://rinkeby.etherscan.io/address/0x8268529c16727cf9a6eF2Ec3f5964A6246752d5f)
* MeemAdminFacet: [0x68183E5636564df820F1CF4Bd0050ffb6F22D763](https://rinkeby.etherscan.io/address/0x68183E5636564df820F1CF4Bd0050ffb6F22D763)
* MeemBaseFacet: [0xD73438CF2c2D3Fcb377ADAb6bA0d591e58565273](https://rinkeby.etherscan.io/address/0xD73438CF2c2D3Fcb377ADAb6bA0d591e58565273)
* MeemPermissionsFacet: [0x41C3ed7Afb404B664E04Da7510047c359dd39d0A](https://rinkeby.etherscan.io/address/0x41C3ed7Afb404B664E04Da7510047c359dd39d0A)
* MeemQueryFacet: [0x16Abd7CbeC0967aAf2738c19b44Ef4500654478B](https://rinkeby.etherscan.io/address/0x16Abd7CbeC0967aAf2738c19b44Ef4500654478B)
* MeemSplitsFacet: [0x9f8A5A4B5F7763fD8E0782aa0AE07a3F3D2fD315](https://rinkeby.etherscan.io/address/0x9f8A5A4B5F7763fD8E0782aa0AE07a3F3D2fD315)

## Source Code

[https://github.com/meemproject/meem-contracts](https://github.com/meemproject/meem-contracts)
