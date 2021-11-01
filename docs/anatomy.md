# Anatomy of a Meem

People create content. That content is copied, remixed, shared, and inspires others.

Meems define the way that we as creators allow others to create.

## Nomenclature

#### Content Creator

Artist, coder, musician, blogger, influencer ... you.

Content Creators should own their content, set permissions on that content, inspire others, and profit from derivative works.

#### MeemDAO

A collective of Content Creators building the web3 future. We work together to design, develop, and evangelize the web3 future where content is not centralized, controlled, and gated behind large corporations. [Join us](https://meems.typeform.com/to/qQaM6q04) in building a better web.

#### Meem Smart Contract

This is the Solidity smart contract code that is deployed on the blockchain that we interact with to create, share, set property rights, transfer, etc. our Meem NFTs.

#### Meem / Meem NFT

A Meem is any NFT that is minted using the Meem Smart Contract. A Meem may have a Parent, and/or Children

#### Wrapped NFT / wNFT

A wNFT is an NFT that is "wrapped" into the Meem protocol. For example, you bought a [Nouns NFT](https://nouns.wtf/) and now you want to allow others to remix that NFT that you own. You can wrap your existing owned Noun onto the Meem Smart Contract.

**You still own your original NFT**. You don't transfer anything. Instead, you use [meem.wtf](https://meem.wtf) to create a clone of your NFT and you assign property rights to the clone. Now, you own your original NFT *AND* a Meem NFT that copies the metadata of your original.

Others may copy or remix your Meem wNFT based on the permissions you've set.

#### Parent

A Parent can have children. A parent might have a parent of their own.

#### Root

The OG parent. The root is the original parent of parent of parent (etc.) that the Meem is based on. In the case of a wNFT, the Root will be the contract address of the original, even if there are several generations of Meems.

## Meem (as represented in our data)

A **Meem** is made up of:

* `address owner` - The owner of the Meem. The wallet that holds this Meem NFT
* `Chain chain` - The chain of the parent contract NFT.
* `address parent` - The parent contract address NFT
* `uint256 parentTokenId` - The parent contract address tokenId for the NFT
* `address root` - The root contract address NFT
* `uint256 rootTokenId` - The root contract address tokenId for the NFT
* `MeemProperties properties` - The properties that apply to this NFT
* `MeemProperties childProperties` - The properties that will automatically be set on any children of this Meem

#### `Chain`

Enum denoting the blockchain where the parent lives.

* Ethereum = `0`
* Polygon = `1`
* Cardano = `2`
* Solana = `3`

#### Meem Properties (`MeemProperties`)

The properties define permissions and limitations that you set on your Meem.

* `int256 totalChildren` - The total number of children that will be allowed to be created. `-1` for unlimited.
* `address totalChildrenLockedBy` - Locks the total children so that it can never be changed. Use the zero-address if not locked.
* `int256 childrenPerWallet` - The number of children that a single wallet can hold. `-1` for unlimited.
* `address childrenPerWalletLockedBy` - Lock the number of children per wallet. Use the zero-address if not locked.
* `MeemPermission[] copyPermissions` - Defines the circumstances under which this Meem can be copied.
* `MeemPermission[] remixPermissions` - Defines the circumstances under which this Meem can be remixed.
* `MeemPermission[] readPermissions` - Defines the circumstances under which this Meem can be viewed.
* `address copyPermissionsLockedBy` - Lock the copy permissions. Use the zero-address if not locked.
* `address remixPermissionsLockedBy` - Lock the remix permissions. Use the zero-address if not locked.
* `address readPermissionsLockedBy` - Lock the read permissions. Use the zero-address if not locked.
* `Split[] splits` - The addresses that should receive royalties when there is a sale.
* `address splitsLockedBy` - Lock the splits. Use the zero-address if not locked.

#### Meem Permission (`MeemPermission`)

* `Permission permission` - The permission this applies to.
* `address[] addresses` - Array of addresses (if applicable) for this permission.
* `uint256 numTokens` - The number of tokens required (if applicable) for this permission.
* `address lockedBy` - If this permission is locked and can not be changed. If not set, use the zero-address.

#### `Permission`

Enum denoting the type of permission

* Owner = `0`
  * Only the token owner has permission. `addresses` and `numTokens` are ignored.
* Anyone = `1`
  * Anyone has permission. `addresses` and `numTokens` are ignored.
* Addresses = `2`
  * Only these wallet `addresses` have permission. `numTokens` is ignored.
* Holders = `3`
  * Only holders of tokens at `addresses` with at least `numTokens` have permission

#### `Split`

Represents a wallet that should receive royalties when a sale occurs.

* `address toAddress` - The address that should receive a percentage of the sale.
* `uint256 amount` - The amount that should be received *in basis points*. (5% == 500)
* `address lockedBy` - Locks this split so it can't be changed. If not locked, use the zero-address

