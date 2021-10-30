# Contract Ownership

Part of the `OwnershipFacet`

## Methods

### `owner()`

Retrieve the contract owner address

**Returns:** `address`

### `transferOwnership(address newOwner)`

Requires sender to be the current owner.

Transfer ownership to a new address

## Examples

```js
const ownership = await (await ethers.getContractFactory('OwnershipFacet')).attach('<Proxy Address>')
const owner = await ownership.owner()
```

