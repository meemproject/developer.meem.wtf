# Meem Permissions

Part of the `MeemPermissionsFacet`

## Methods

Some methods below mention the **zero-address**. This is a special address that noone owns. In our usage, we use it to denote address fields that have not been set.

The **zero-address** is: `0x0000000000000000000000000000000000000000`

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

## Examples

```js
const meem = await (await ethers.getContractFactory('MeemPermissionsFacet')).attach('<Proxy Address>')

```

