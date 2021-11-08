# Meem Admin

Part of the `MeemAdminFacet`

## Methods

### `setTokenCounter(uint256 tokenCounter)`

Set the token counter

**Parameters:**
* `uint256 tokenCounter` - The new token counter

### `setContractURI(string newContractURI)`

Set the contract URI

**Parameters:**
* `string newContractURI` - The new contract URI

### `setChildDepth(uint256 newChildDepth)`

Set the max depth of children that can be minted

**Parameters:**
* `uint256 newChildDepth` - The child depth

### `setNonOwnerSplitAllocationAmount(uint256 amount)`

Set the minimum non-owner split allocation (in basis points)

**Parameters:**
* `uint256 amount` - The new minimum non-owner split allocation


## Examples

```js
const meemAdmin = await (await ethers.getContractFactory('MeemAdminFacet')).attach('<Proxy Address>')
```

