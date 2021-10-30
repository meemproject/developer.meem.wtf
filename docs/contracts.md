# Smart Contracts

In order to facilitate future upgrades to Meems, we use a combination of [UUPS Proxy](https://docs.openzeppelin.com/contracts/4.x/api/proxy#UUPSUpgradeable) and [EIP-2535 Diamonds](https://eips.ethereum.org/EIPS/eip-2535).

## Implementation

**The main proxy contract is the address you should use**. Facet addresses will change when the contract is upgraded.

## Smart Contract Quick Links

### Polygon

**Coming Soon**

### Rinkeby Testnet

**Main Proxy Contract: [0xEBf9B4f3AeEEb1aEFbAf535DC8E353809a7Df6D4](https://rinkeby.etherscan.io/address/0xEBf9B4f3AeEEb1aEFbAf535DC8E353809a7Df6D4)**

#### Facets

* DiamondCutFacet: [0x5A6A75a1Ea30f1D564bb36DE45292a236d74A98E](https://rinkeby.etherscan.io/address/0x5A6A75a1Ea30f1D564bb36DE45292a236d74A98E)
* Diamond: [0x197b0716c9e260f9c7bC48781A7e59d6Dc15E513](https://rinkeby.etherscan.io/address/0x197b0716c9e260f9c7bC48781A7e59d6Dc15E513)
* DiamondLoupeFacet: [0x27CCb33F5b7eec52A85c5dfE6eec4388fCe349E9](https://rinkeby.etherscan.io/address/0x27CCb33F5b7eec52A85c5dfE6eec4388fCe349E9)
* MeemFacet: [0x80897317b9C8D9273b451688121D471c46844d51](https://rinkeby.etherscan.io/address/0x80897317b9C8D9273b451688121D471c46844d51)

## Source Code

[https://github.com/meemproject/minty-nft](https://github.com/meemproject/minty-nft)