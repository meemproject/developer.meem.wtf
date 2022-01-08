# Meem Smart Contracts

In order to facilitate future upgrades to Meems, we use [EIP-2535 Diamonds](https://eips.ethereum.org/EIPS/eip-2535).

## Implementation

**The main proxy contract is the address you should use**. Facet addresses will change when the contract is upgraded.

## Smart Contract Quick Links

### ABI / Typescript

Full ABI with all functions: [Meem.json](https://raw.githubusercontent.com/meemproject/meem-contracts/master/types/Meem.json)

Typechain Types: [https://github.com/meemproject/meem-contracts/tree/master/types/ethers-contracts](https://github.com/meemproject/meem-contracts/tree/master/types/ethers-contracts)

### Polygon (Live Contract)

**Main Proxy Contract: [0x82aC441F3276ede5db366704866d2E0fD9c2cFA8](https://polygonscan.com/address/0x82aC441F3276ede5db366704866d2E0fD9c2cFA8)**

#### Facets

* AccessControlFacet: [0xB5e8573331888047B1fc72f1d05444Cc1eEe4Ae9](https://polygonscan.com/address/0xB5e8573331888047B1fc72f1d05444Cc1eEe4Ae9)
* ERC721Facet: [0xf5a0fD628AFe07D8c3736762Bd65Ae009F23e335](https://polygonscan.com/address/0xf5a0fD628AFe07D8c3736762Bd65Ae009F23e335)
* InitDiamond: [0x65c7CA5057E5DAbf1a9D8dB34151a9C29a604A3F](https://polygonscan.com/address/0x65c7CA5057E5DAbf1a9D8dB34151a9C29a604A3F)
* MeemAdminFacet: [0x4f999BE4DCC960c4Aa578728cdA1E8d8f53e9529](https://polygonscan.com/address/0x4f999BE4DCC960c4Aa578728cdA1E8d8f53e9529)
* MeemBaseFacet: [0xBA78291b5f511F6F03D7646bCd11Ac9eC058EDeB](https://polygonscan.com/address/0xBA78291b5f511F6F03D7646bCd11Ac9eC058EDeB)
* MeemPermissionsFacet: [0x14f6E03432424c88Bdb0252F670c70DB8eA37A00](https://polygonscan.com/address/0x14f6E03432424c88Bdb0252F670c70DB8eA37A00)
* MeemQueryFacet: [0x9594D6eC22ad72400a93Ad2235f649E1cF12213E](https://polygonscan.com/address/0x9594D6eC22ad72400a93Ad2235f649E1cF12213E)
* MeemSplitsFacet: [0x545De2D3FFeF9e8eCAEB6dE74460C7FecB2313F5](https://polygonscan.com/address/0x545De2D3FFeF9e8eCAEB6dE74460C7FecB2313F5)

### Rinkeby (Testnet Contract)

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
