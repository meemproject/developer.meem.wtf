# Meem Base

Part of the `MeemBase`

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


### `tokenIdsOfOwner(address owner)`

**Returns:** `uint256[]` - Array of tokenIds that are owned by this address.

Get all tokenIds owned by an address

### `childrenOf(uint256 tokenId)`

**Returns:** `uint256[]` - Array of tokenIds that are children of this token.

Get all the children of a token.

### `numChildrenOf(uint256 tokenId)`

**Returns:** `uint256` - Returns the number of children of this token

Get the number of children of a token

### `getMeem(uint256 tokenId)`

**Parameters:**
* `uint256 tokenId` - The tokenId to get

**Returns:** `Meem` - Returns the entire Meem object that defines properties / splits.

### `isNFTWrapped(address contractAddress, uint256 tokenId)`

Checks if an NFT has already been "wrapped" / minted as a Meem

**Parameters:**
* `address contractAddress` - The address of an ERC721 contract
* `uint256 tokenId` - The tokenId in the contract

**Returns:** `bool` - Whether the NFT has been minted as a Meem


## Examples

```js
const meem = await (await ethers.getContractFactory('MeemBaseFacet')).attach('<Proxy Address>')

```

