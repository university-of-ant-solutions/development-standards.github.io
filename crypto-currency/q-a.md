---
description: question and answer
keywords: scrum, product, development, process
title: Scrum
---

1. How much does it cost to use a contract?

Still new to ethereum and would like to know the price for a contract.

- Answer

The total cost of a transaction that creates a contract or executes a contract is based on 2 factors:

gasUsed is the total gas that is consumed

gasPrice specified in the transaction

Total cost = gasUsed * gasPrice

gasUsed
Each operation in the Ethereum Virtual Machine (EVM) [was assigned a number of how much gas it consumes](https://ethereum.stackexchange.com/q/52/42).  gasUsed is summing up all the gas for all the operations executed. There is a spreadsheet which offers a glimpse to some of the analysis behind them.

For estimating [gasUsed](https://ethereum.stackexchange.com/q/197/42), there is an [estimateGas API with some caveats](https://ethereum.stackexchange.com/q/266/42).

gasPrice
A user constructs and signs a transaction, and each user may specify whatever gasPrice they desire, this includes zero. However, the Ethereum clients launched at Frontier had a default gasPrice of 0.05e12 wei. As miners optimize for their revenue, if most transactions are being submitted with a gasPrice of 0.05e12 wei, it would be difficult to convince a miner to accept a transaction that specified a lower, or zero, gasPrice. How the default was chosen is asked in this [question](question).

Example
Let's take a contract that just adds 2 numbers. From the spreadsheet above ADD consumes 3 gas.

The approximate cost, using the default gas price, would be:

3 * 0.05e12 = 1.5e11 wei

Since 1 Ether is 1e18 wei, the total cost would be 0.00000015 Ether.

This is a simplification since it ignores some costs, such as the cost of passing the 2 numbers to contract, before they can even be added.

- [1.0 gas costs](https://docs.google.com/spreadsheets/d/1m89CVujrQe5LAFJ8-YAUCcNK950dUzMQPMJBxRtGCqs/edit#gid=0)
