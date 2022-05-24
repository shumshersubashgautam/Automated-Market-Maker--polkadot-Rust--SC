# Automated-Market-Maker--polkadot-Rust--SC
Tutorial Link: Create an AMM on Polkadot using Ink!

Description:

The tutorial will guide the developers to build an Automated Market Maker (AMM) dApp on a substrate-based chain with contract-pallet support. It will explain the internal working of an AMM and how to develop one using ink!, a Rust-based embedded Domain Specific Language (eDSL), and deploy it on a public testnet (Jupiter A1 of Patract) using https://polkadot.js.org/apps. It will also illustrate how to integrate the smart contract with a react application using polkadot.js module and polkadot{.js} browser extension.

The AMM will have the following features: Provide, Withdraw and Swap. It will also support trading fees to incentivize liquidity providers to add liquidity and slippage tolerance to protect traders from market fluctuation. To keep things simple, The AMM doesn't implement routing and, hence it will deal with only two tokens at a time. The AMM will maintain its own internal mapping that stores the balance of accounts instead of dealing with the external tokens.
Prerequisites
You should be familiar with Rust and ReactJS
It will be much easier to follow this tutorial if you have completed the ink! beginners guide 
is here https://docs.substrate.io/tutorials/v3/ink-workshop/pt1/
Requirements
Node.js v10.18.0+
Polkadot{.js} extension on your browser
Ink! v3 setup

What is an AMM?
Automated Market Maker(AMM) is a type of decentralized exchange which is based on a mathematical formula of price assets. It allows digital assets to be traded without any permissions and automatically by using liquidity pools instead of any traditional buyers and sellers which uses an order book that was used in traditional exchange, here assets are priced according to a pricing algorithm.
For example, Uniswap uses p * q = k, where p is the amount of one token in the liquidity pool, and q is the amount of the other. Here “k” is a fixed constant which means the pool’s total liquidity always has to remain the same. For further explanation let us take an example if an AMM has coin A and Coin B, two volatile assets, every time A is bought, the price of A goes up as there is less A in the pool than before the purchase. Conversely, the price of B goes down as there is more B in the pool. The pool stays in constant balance, where the total value of A in the pool will always equal the total value of B in the pool. The size will expand only when new liquidity providers join the pool.
Implementing the smart contract
Move to the directory where you want to create your ink! project and run the following command in the terminal which will create a template ink! project for you.
cargo contract new amm
Move inside the amm folder and replace the content of lib.rs file with the following code. We have broken down the implementation into 10 parts.
// Part 1. Define Error enum 

    // Part 2. Define storage struct 

    // Part 3. Helper functions 

    impl Amm {
        // Part 4. Constructor

        // Part 5. Faucet

        // Part 6. Read current state

        // Part 7. Provide

        // Part 8. Withdraw

        // Part 9. Swap
    }

    // Part 10. Unit Testing
}
Deploying the smart contract

cargo +nightly contract test

cargo +nightly contract build --release
 
 
