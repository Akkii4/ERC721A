# ERC721A

AN IMPROVED ERC721 IMPLEMENTATION

### Who's the new kid in token : ERC721A ?

Untill January 2022 many projects were using the standard Openzepplin ERC721 & it's extensions , but something came up on January 12 @ 10:00AM PST & grabbed everyone eyes & that's none other than The Azuki (the NFT Collection) firstly implemented it's smart contract with indicating ERC721A as base contract , was it a typo? NO.

### So why the need of : ERC721A ?

Wasn't ERC721 good enough ? YES it is , but just good as due to the NFT craze and choking Blocks in Ethereum Blockchain the gas price is reaching new highs & it's almost being impossible for retail to economically mint the NFTs especially in batches(more than one)

![Gas savings being offered by ERC721A as compared to ERC721 Enumerable.](https://camo.githubusercontent.com/d13739d5ecfd5dc882b0cb7089a770b55f4bb1a1abf98067b94e1c21864fb261/68747470733a2f2f7062732e7477696d672e636f6d2f6d656469612f464964494c4b7056514145515f35553f666f726d61743d6a7067266e616d653d6d656469756d)


### How it does that ?

    1. Reduces the unused space, which is used to store metadata of NFTs.
    2. Updating the owner’s balance once per batch mint request, instead of per minted NFT
    3. Updating the owner data once per batch mint request, instead of per minted NFT

### But then we should throw standard ERC721 ?

If ERC721A is so good that it solves all of the ERC721 problem then why don't dump the standard & instead use ERC721A,
because there is a downside to it as well.

The problem is transferring of NFT while batch minting cost more gas than the standard one as transferring a tokenID that does not have an owner address,
the contract must create actions that include all tokenID’s in order to verify the original NFT owner.

### Solution

Transferring costs minimizes if transfer takes place after minting the maximum allowed number of NFT when releasing an entire batch.
