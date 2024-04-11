# Ore CLI 2 RPC

A custom command line interface for the Ore program that utilizes **2 rpcs**, one for sending the **sendTransaction** method, the other one to do all the rest. (Actually using v0.4.12-alpha ore cli version)

## Requirements

### Install Rust

To install my custom Ore CLI, you will need to have the **Rust** programming language installed. You can **install Rust** by following the instructions on the [Rust website](https://www.rust-lang.org/tools/install).

```sh
curl https://sh.rustup.rs -sSf | sh
```

### Install Solana

If you don't have Solana client installed yet, run the following commands

```sh
sh -c "$(curl -sSfL https://release.solana.com/v1.18.4/install)"
```

### Install the custom rpc

Install the ore client 2 rpc

```sh
cargo install ore-cli-2rpc
```

## How to use ?

Use the command **ore2rpc** instead of **ore**.

This custom ore client accept one more option that is the rpc2 option. The rpc2 option will be the rpc who will receive the sendTransaction method. The other rpc will receive all the others request like getSignaturesStatuses, getLatestBlockHash, getVersion, etc...

<em>You can use the same rpc in both variables</em>

```sh
$rpc1="url_rpc_1"
$rpc2="url_rpc_2"

ore2rpc \
    --rpc $rpc1 \
    --rpc2 $rpc2 \
    --keypair ~/.config/solana/id.json \
    --priority-fee 10000 mine 
```

Expect around ~2500 requets per hour for one command.

## Warnings

This project is developed by me and I am **not** a professional Rust developer, so use with **caution**. Always monitor your rpc credits.

## Donation & Tips

I am accepting donations and tips at this solana adress (ORE, SOL, USDC) :
**AwdcrnSqdzdEdsGkx2f2zxNA4dENBDjMdpBtMtVDCrKc**