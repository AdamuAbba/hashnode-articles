### 📜Objective

The goal of this article is to help you

- understand Bitcoin addresses
  - Legacy (P2PKH)
  - Nested SigWit (P2SH)
  - Native SegWit (Bech32)
  - Taproot (P2TR)
- Bitcoin Transactions

### 📜 Introduction

Welcome to the second part of the series. incase if you haven't already gone over the first part, please ensure you go over it [permlink here](#) so you would have a better understanding of this part.

In this part we'll be talking about the different bitcoin addresses and what forms of improvement they brink into the Bitcoin ecosystem. we may get a little technical in this article but hey it's nothing we can't handle right?

![wink](https://media.giphy.com/media/l41JU9pUyosHzWyuQ/giphy.gif)

Now let's get to it shall we?

### Understanding Bitcoin addresses

Now we know that the Bitcoin address is a fundamental part of the Bitcoin ecosystem that ensures transaction validations, generation of digital signatures and a host of important functionalities.

### Why do we have different Bitcoin address types?

Well around 2016 and 2017, there was a discussion or debate around the Bitcoin `Block size` which was `1 mb` per block and so only a limited amount of transactions could be added to a block. The accepted solution was to take a part of the transaction called the `witness data` and move it to a second layer on the blockchain there by allowing more space for transactions on the main block and increasing the block size to

Let's look at the types of Bitcoin Addresses and why they are important.

### Legacy Address a.k.a Pay-to-Public-Key-Hash (P2PKH)

This is the oldest of all Bitcoin addresses. In fact, it is the original Bitcoin address and has a prefix of `1`.

Quick Facts

- They are accountable, stable and universally supported.
- Transactions via Legacy addresses have are large in size, meaning they take up more block space.
- transactions from Legacy addresses have high transaction fees due to the size of the transactions
- Legacy addresses are `not` SegWit compatible what this means is that on the Bitcoin network, only Legacy addresses can carry out transactions with with each other i'e send and and receive BTC.

### Nested SegWit a.k.a Pay-to-Script-Hash (P2SH)

This address is an improvement over `Legacy addresses` the implements better scalability, security and smaller block size their by enabling multiple transactions on the blockchain without having too much of an impact on the the Bitcoin blockchain size. it has a prefix of `3`

Quick Facts

- They have cheeper transaction fees and enhanced security over `Legacy addresses` thy achieve this through multi-signature capabilities.
- Nested SegWit addresses have cross compatibility meaning transactions can be carried out between Nested SegWit and other types of Bitcoin Addresses.

### Native SegWit a.k.a pay-to-witness-public-key-hash (Bech32)

This type of Bitcoin address has a prefix of "bc1q" and it has an upgrade to the Nested SegWit. The Native SegWit is also compatible with most wallets and exchanges by default.

### Taproot a.k.a Pay-to-Taproot (P2TR)

This Bitcoin Address type has a prefix pf "bc1p" and has the lowest transaction fees of all existing Bitcoin Address types.

### Conclusion

The best part about an open blockchain system is how it is community driven and so over time improvements are welcomed and accepted.

### Useful links

- [Bitcoinbook](https://github.com/bitcoinbook/bitcoinbook)
- [Soren Azorian | Demystifying Bitcoin Address Types: Legacy, SegWit, Native SegWit, and Taproot](https://www.linkedin.com/pulse/demystifying-bitcoin-address-types-legacy-segwit-native-soren-azorian/)
