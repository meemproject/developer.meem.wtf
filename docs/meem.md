# Meem

Part of the `MeemFacet`

Extends the entire concept of an NFT to include advanced property rights.

## Methods

Some methods below mention the **zero-address**. This is a special address that noone owns. In our usage, we use it to denote address fields that have not been set.

The **zero-address** is: `0x0000000000000000000000000000000000000000`

### `mint(<See Params Below>)`

**Parameters:**
* `address to` - The address that will receive the newly minted NFT
* `string mTokenURI` - The tokenURI pointing to the metadata
* `Chain chain` - The chain of the parent NFT
* `address parent` - The contract address of the direct parent NFT. This could be the Meem contract address if we're creating a child of an existing Meem. If this is an original work, use the zero-address.
* `address parentTokenId` - The tokenId in the parent contract. If this is an original, use 0.
* `address root` - The original, top-level contract address this Meem is derived from. If this is an original, use the zero-address.
* `uint256 rootTokenId` - The original, top-level contract tokenId this Meem is derived from. If this is an original, use 0.
* `MeemProperties mProperties` - The properties of this Meem. See [Anatomy of a Meem](anatomy.md) for more info.
* `MeemProperties mChildProperties` - The properties that children of this Meem will be assigned at creation. See [Anatomy of a Meem](anatomy.md) for more info.

Requires that sender has the MINTER_ROLE

### `mintChild(<See Params Below>)`

**Coming Soon**

Mint a child from an existing Meem based on the permissions that have been set in the parent.

### `getRaribleV2Royalties(uint256 tokenId)`

Meems are compatible with the [Rarible Royalties Standard](https://medium.com/rarible-dao/rarible-nft-royalties-in-your-custom-smart-contract-b07550e89ef4) which allows defining of which addresses should receive royalties as part of a sale **on a per-token basis**. This standard fits perfectly with Meems which define "Splits". See [Anatomy of a Meem](anatomy.md) for more info.

### `nonOwnerSplitAllocationAmount()`

**Returns:** `uint256` - The amount (in basis points) that must be allocated to an address that is not the token owner.

Since Meems are all about derivative works and inspiration, we require that a certain amount of future royalties be pointed at another address. This could be the address of the creator who inspired the work, or it could be the address of a person or organization that you want to support. We are all creators, but we're also all inspired by others.

### `setNonOwnerSplitAllocationAmount(uint256 amount)`

**Parameters:**
* `uint256 amount` - The new amount to require (in basis points). This must not exceed 100% (10000 in basis points)

Requires the sender have the DEFAULT_ADMIN_ROLE

Update the required amount that must be pointed at non-owner addresses when minting a Meem.

### `tokenIdsOfOwner(address owner)`

**Returns:** `uint256[]` - Array of tokenIds that are owned by this address.

Get all tokenIds owned by an address

### `childrenOf(uint256 tokenId)`

**Returns:** `uint256[]` - Array of tokenIds that are children of this token.

Get all the children of a token.

### `numChildrenOf(uint256 tokenId)`

**Returns:** `uint256` - Returns the number of children of this token

Get the number of children of a token

### `setTotalChildren(uint256 tokenId, int256 newTotalChildren)`

**Parameters:**
* `uint256 tokenId` - The tokenId to update the total children for
* `int256 newTotalChildren` - The new number of children to allow to be created from this Meem. For unlimited, set to -1. *This number must be greater than or equal to the current number of children.*

Requires the sender is the token owner

### `lockTotalChildren(uint256 tokenId)`

**Parameters:**
* `uint256 tokenId` - The tokenId to lock the total children for

Requires the sender is the token owner

**Careful: This action is permanent.** Once locked, the total number of children can never be adjusted. This fixes the total number of children that will ever be created from this Meem.

### `setChildrenPerWallet(uint256 tokenId, int256 newTotalChildren)`

**Parameters:**
* `uint256 tokenId` - The tokenId to update the children per wallet for
* `int256 newTotalChildren` - The new number of children per wallet to allow to be created from this Meem. For unlimited, set to -1. *Previously minted children are not affected by this.*

Requires the sender is the token owner

### `lockChildrenPerWallet(uint256 tokenId)`

**Parameters:**
* `uint256 tokenId` - The tokenId to lock the children per wallet for

Requires the sender is the token owner

**Careful: This action is permanent.** Once locked, the children per wallet can never be adjusted.

### `addPermission(<See Params Below>)`

**Parameters:**
* `uint256 tokenId` - The tokenId to add the permission to
* `PropertyType propertyType` - Is this being set for this Meem or for future-minted child Meems? *0 == this Meem*, *1 == Children*
* `MeemPermission permission` - The permission

Requires the sender is the token owner

### `removePermissionAt(<See Params Below>)`

**Parameters:**
* `uint256 tokenId` - The tokenId to remove the permission from
* `PropertyType propertyType` - Is this being set for this Meem or for future-minted child Meems? *0 == this Meem*, *1 == Children*
* `uint256 idx` - The index of the permission to remove

Requires the sender is the token owner

### `updatePermissionAt(<See Params Below>)`

**Parameters:**
* `uint256 tokenId` - The tokenId to update the permission
* `PropertyType propertyType` - Is this being set for this Meem or for future-minted child Meems? *0 == this Meem*, *1 == Children*
* `uint256 idx` - The index of the permission to update
* `MeemPermission permission` - The permission

Requires the sender is the token owner

Replaces the *MeemPermission* at the specified index

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

### `getMeem(uint256 tokenId)`

**Parameters:**
* `uint256 tokenId` - The tokenId to get

**Returns:** `Meem` - Returns the entire Meem object that defines properties / splits.

### `childDepth()`

**Returns:** `uint256` - The current child depth allowed

The child depth defines how far *down the tree* of Meems are allowed to be minted. At launch only wrapping existing NFTs will be supported. Later, children will be allowed, then children of children and so on.

### `setChildDepth(uint256 newChildDepth)`

**Parameters:**
* `uint256 newChildDepth` - The new depth to allow

Requires the sender have the DEFAULT_ADMIN_ROLE

Updates the child depth to allow additional levels of Meems

## Examples

```js
const meem = await (await ethers.getContractFactory('MeemFacet')).attach('<Proxy Address>')

```

