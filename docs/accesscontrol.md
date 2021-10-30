# Access Control

Part of the `AccessControlFacet`

## Methods

### `DEFAULT_ADMIN_ROLE()`

Role for the contract admin.

**Returns:** `bytes32`
* The hashed representation of the role

### `MINTER_ROLE()`

Role that allows minting of root level Meems

**Returns:** `bytes32`
* The hashed representation of the role

### `grantRole(address user, bytes32 role)`

Requires sender role: DEFAULT_ADMIN_ROLE

**Parameters:**
* `address user` - The address who should be granted to role
* `bytes32 role` - The role that should be granted

### `revokeRole(address user, bytes32 role)`

Requires sender role: DEFAULT_ADMIN_ROLE

**Parameters:**
* `address user` - The address who should be revoked
* `bytes32 role` - The role that should be revoked

### `hasRole(address user, bytes32 role)`

Check if the given user has a role

**Parameters:**
* `address user` - The address to check
* `bytes32 role` - The role to check

## Examples

```js
const accessControl = await (await ethers.getContractFactory('AccessControlFacet')).attach('<Proxy Address>')
const minterRole = await accessControl.MINTER_ROLE()

await accessControl.grantRole('0x5E4844117f7D8f0cb6Ee9E2b01B14347a4fbB426', minterRole)

await accessControl.hasRole('0x5E4844117f7D8f0cb6Ee9E2b01B14347a4fbB426', minterRole)
```

