# MCG Signal methodology

This repository tells how MCG Signal counts each value it shows. Each change is in [CHANGELOG.md](CHANGELOG.md).

## Methods

Each document answers one question.

| Question | Document |
| --- | --- |
| What is one token, and what is one X account? | [docs/identity.md](docs/identity.md) |
| What do we record for a value, and how do we prove it? | [docs/values.md](docs/values.md) |
| What is a burn, and what is not a burn? | [docs/burns.md](docs/burns.md) |

## Independence

1. We use one method for all projects.
2. An appearance on MCG Live changes no value, rank or label.
3. No project pays for a place, a rank or a label in the data.
4. Anyone can report an error with proof from the chain. We correct it in public.

## Limits

We do not yet give a public way to repeat our reads, and our pages do not show the block of each value yet. When we give a block, in the changelog or in an answer to an issue, anyone with a node of that chain can repeat the read. See [how we prove a value](docs/values.md#how-we-prove-a-value).

## Report an error

Open an issue with the ["Data error" form](https://github.com/mcgsignal/methodology/issues/new?template=data-error.yml). Give the proof from the chain. We answer in the issue.

## Change this repository

ICM Analytics maintains this repository. To change it, follow [CONTRIBUTING.md](https://github.com/mcgsignal/.github/blob/main/CONTRIBUTING.md). This repository adds two types and two rules:

| Type | Use it when |
| --- | --- |
| `method` | A rule that counts a value changes. |
| `data` | A value was wrong and the rule stays the same. |

- A `method` or `data` change adds an entry to [CHANGELOG.md](CHANGELOG.md): what changed and why.
- ICM Analytics approves each `method` change before the merge.

Examples: `method: count a bridge fee as a burn`, `data: move 12 transfers from bridge exits back to burns`.

## License

The text in this repository is under [CC BY 4.0](LICENSE). You can copy and change it, also for commercial use, if you credit MCG Signal. The license is for this text only. Data that we publish has its own terms. The terms of the token list are at [icm-analytics.com/label/terms](https://icm-analytics.com/label/terms/).
