# How we record and prove a value

## What we record for each value

| Field | What it means |
| --- | --- |
| Chain | The chain we read, for example Robinhood Chain (chain ID 4663). |
| Block | The block number of the read. |
| Time | The UTC time of that block. |
| Source | Where the value comes from, for example a read of the chain. |
| Coverage | The first and last block or day that the value covers. |

## Where we read the chain

We read each chain from our own nodes or from an indexer that our team runs.

## How we prove a value

A blockchain gives one answer at one block. When we prove a value, we read it at a fixed block and keep the block hash with the result. Anyone can repeat the same read at the same block and get the same answer.

## Gaps

When a source does not cover a period, we show the gap. We never fill it with an estimate. A missing value is not zero.

## Prices

A USD value is a valuation: the number of tokens times a price at one time. It is not the amount that somebody paid.
