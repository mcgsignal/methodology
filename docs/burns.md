# Burns

## What is a burn

A burn is a transfer of a token to one of these two addresses:

- the zero address, `0x0000000000000000000000000000000000000000`;
- the dead address, `0x000000000000000000000000000000000000dEaD`.

A standard token burn function also makes a transfer to the zero address.

## What the Burn Tracker shows

| Item | Rule |
| --- | --- |
| Listing minimum | A token is on the list when its burns have an estimated value of 1 ETH or more, or the same value in USD. For the periods 24 hours, 7 days and 30 days, we count the burns of the last 30 days. For the period "all time", we count all burns. |
| Periods | 24 hours, 7 days, 30 days and all time. |
| Burned | The tokens that went to the zero address or the dead address in the period. |
| Burn days | The number of UTC dates with one burn or more, in the 30 days that end on the date of the data. |
| Estimated value | The burned tokens at the current price of the token. The page shows the 24-hour value only when the liquidity of the token supports the price. For what a USD value means, see [prices](values.md#prices). |

## What is not a burn

**A bridge exit is not a burn.** Some bridges remove a token on one chain and create it again on another chain. The supply did not go down: it moved. We do not count these transfers as burns.

We prove a bridge exit in one of these ways:

| Bridge type | How we prove the exit |
| --- | --- |
| LayerZero OFT tokens | The bridge sends a message for each exit. We find the message for the same transaction, and we compare the amount in the message with the amount that left. |
| Chainlink CCIP token pools | The CCIP explorer shows the message for the same transaction. |
| The chain's token gateway | We read the code of the gateway contract. No outside explorer shows these exits, so the contract code is the only proof. |

When we cannot prove an exit in one of these ways, the transfer stays a burn.

## Limits

- **Dust.** A bridge sends whole units at its own precision. A smaller amount that stays behind is destroyed. This small amount is a real burn, but we count the whole transfer as an exit.
- **A fee that the bridge destroys.** Some bridges destroy a fee with the exit. We do not count this fee as a burn.
