# Identity

## A token is its chain and its contract address

We identify each token by its chain and its contract address, for example `robinhood:0x...`. Many tokens can use the same ticker. Only one token has a given contract address on a given chain.

- **The ticker is a label.** We show it, but we never use it to connect data.
- **When two tokens use the same ticker,** the ticker points to neither of them. You find each token by its contract address.
- **A native coin,** for example NEAR, has no contract address. We identify it by its chain.
- **A project before its token** has no contract address yet. We identify it by its name until the token exists.

## A token that moves

When a project moves to a new contract, we keep two records: the old token and the new token. The old record points to the new one. We never give the old contract's history to the new contract.

## An X account is its user ID

We identify each X account by its numeric user ID. The handle is a label. A handle can change or go to another person. The user ID stays with the account. When a handle and a user ID disagree, the user ID wins.
