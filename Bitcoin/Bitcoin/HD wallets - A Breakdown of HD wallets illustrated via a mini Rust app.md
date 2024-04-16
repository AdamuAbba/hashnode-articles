## 📜Objective

The goal of this article to help you

- Install and Setup your rust environment
- Learn how to build a very simple rust CLI app to help us understand Bitcoin HD wallet
- Learn about HD wallets
- Advantages and Disadvantages of HD wallets
- Learn a bit about Bip32 and it's underlying standards
  - Bip39
  - Bip44
  - Bip49
  - Bip84

## Requirements & specs

### Requirements and specs

- Some understanding of the Bitcoin ecosystem
- Some basic basic knowledge of the Rust Language
- The rust installed and configured on your machine

### ⚙️ My system specs

- Machine: HP elite book
- Operating System: Ubuntu 22.04.4 LTS
- terminal: Gnome Terminal
- shell: ZSH
- Editor: Neovim

## 📜 Introduction

So you recently came across HD wallets and you're a bit curious as to why they are so awesome. furthermore, you're the kind of guy looking for a mini pet rust project to get your hands dirty with some bitcoin rust development

## Setting up your rust and bootstrapping your CLI app

setting up rust on your machine can be done via [rustup](https://rustup.rs/) and is as easy as running the command bellow and following through the prompts if you are on an ubuntu machine or a Mac

```zsh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Now to bootstrap a new rust project run the command below from a convenient directory

```zsh
cargo new shy-bit-rust
```

Let's open up and run the app

```zsh
cd shy-bit-rust && nvim . && cargo run
```

## What are HD wallets

Hierarchical Deterministic wallets as defined by the Bip32 standard are a kind of cryptocurrency wallet that allows for generation of keys from a single seed or mnemonic phrase

## Advantages of HD wallets

Now that we know what we have some idea of what HD wallets are, let's look at some advantages.

### Deriving Unlimited Wallet Addresses

HD wallets enable the creation of as many addresses as needed, all tied to a single wallet via a child addresses to wallet chain relationship.

### Security & Privacy

HD wallets provide security and protection via the master seed i.e a 12, 18 or 24 word mnemonic phrase from which all the wallet`s private keys are derived.

### Wallet interoperability

One really cool thing about HD wallets is that they can be restored on different devices and wallet applications by simply entering your seed phrase unlike other types of wallets but the only condition is they must support both BIP-39 and BIP-44 standards.

### Costs reductions

### Single point of ownership

A wise totally real Bitcoin philosopher once said...

![wise rick](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExNmdjamRjZGtsMWtzaGk3YzVqcGNma2xhZHBwbHJnYnRmcG1pY3prNSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/1USKMDPjuH4ovL7J5h/giphy.gif)

> "Whoever possesses the private keys owns the wallet."

This is valid because all public keys and addresses can be generated from the private keys.

### Disadvantages of HD wallets

On big and obvious concern of working with HD wallets is the fact that the security of your seed or mneomonic phrase getting compromised would naturally imply the lost of ownership to your wallet

### Conclusion