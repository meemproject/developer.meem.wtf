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

#### Parent

A Parent can have children. A parent might have a parent of their own.

#### Root

The OG parent. The root is the original parent of parent of parent (etc.) that the Meem is based on. In the case of a wNFT, the Root will be the contract address of the original, even if there are several generations of Meems.

## Meem (as represented in our data)

A **Meem** is made up of:

* `owner` - The owner of the Meem. The wallet that holds this Meem NFT
* `chain` - The chain of the parent contract NFT.
* `parent` - The parent contract address NFT
* `parentTokenId` - The parent contract address tokenId for the NFT
* `root` - The root contract address NFT
* `rootTokenId` - The root contract address tokenId for the NFT
*