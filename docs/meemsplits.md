# Meem Splits

Part of the `MeemSplitsFacet`

## Methods

Some methods below mention the **zero-address**. This is a special address that noone owns. In our usage, we use it to denote address fields that have not been set.

The **zero-address** is: `0x0000000000000000000000000000000000000000`

### `getRaribleV2Royalties(uint256 tokenId)`

Meems are compatible with the [Rarible Royalties Standard](https://medium.com/rarible-dao/rarible-nft-royalties-in-your-custom-smart-contract-b07550e89ef4) which allows defining of which addresses should receive royalties as part of a sale **on a per-token basis**. This standard fits perfectly with Meems which define "Splits". See [Anatomy of a Meem](anatomy.md) for more info.

### `nonOwnerSplitAllocationAmount()`

**Returns:** `uint256` - The amount (in basis points) that must be allocated to an address that is not the token owner.

Since Meems are all about derivative works and inspiration, we require that a certain amount of future royalties be pointed at another address. This could be the address of the creator who inspired the work, or it could be the address of a person or organization that you want to support. We are all creators, but we're also all inspired by others.

### `addSplit(uint256 tokenId, PropertyType propertyType, Split split)`

**Parameters:**
* `uint256 tokenId` - The tokenId to update
* `PropertyType propertyType` - Is this being set for this Meem or for future-minted child Meems? *0 == this Meem*, *1 == Children*
* `Split split` - The split to add

Requires the sender is the token owner

### `removeSplitAt(uint256 tokenId, PropertyType propertyType, uint256 idx)`

**Parameters:**
* `uint256 tokenId` - The tokenId to update
* `PropertyType propertyType` - Is this being set for this Meem or for future-minted child Meems? *0 == this Meem*, *1 == Children*
* `uint256 idx` - The index of the split to remove

Requires the sender is the token owner

### `updateSplitAt(<See Params Below>)`

**Parameters:**
* `uint256 tokenId` - The tokenId to update
* `PropertyType propertyType` - Is this being set for this Meem or for future-minted child Meems? *0 == this Meem*, *1 == Children*
* `uint256 idx` - The index of the split to remove
* `Split split` - The replacement split

Requires the sender is the token owner

## Examples

```js
const meem = await (await ethers.getContractFactory('MeemSplitsFacet')).attach('<Proxy Address>')

```

