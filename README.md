# Pegasys Tokenlists

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow the specification. The Pegasys community invites you to add your token to our tokenlists!

Mainnet and testnet tokenlist registries are handled independently.

## Adding Your Token to an Existing List

### General Requirements
1. Token should be verified on the [block explorer](https://tanenbaum.io/).
2. Token must be added to a list that it qualifies for:
    <!-- * **[Top 20 Tokenlist](./top20.tokenlist.json)**: Token must be in the top 20 of eligible Syscoin tokens by marketcap. -->
    * **[SB Tokenlist](./ab.tokenlist.json)**: Token must be bridgeable on the Syscoin Bridge.
    * **[DeFi Tokenlist](./defi.tokenlist.json)**: Token must be connected to a DeFi protocol running on Syscoin.
    * **[Tanembaum Tokenlist](./tanembaum.tokenlist.json)**: Token must be a Tanembaum Network token.

## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Here is an example:
    ```json
    {
        "address": "0x0000000000000000000000000000000000000bAe",
        "chainId": 69420,
        "name": "Bae Token",
        "symbol": "BAE",
        "decimals": 18,
        "logoURI": "https://raw.githubusercontent.com/logo.png"
    }
    ```
2. Update the `timestamp` field to the current timestamp.
3. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.


## Creating Your Own List

List creation is encouraged! The Pegasys team wants the community to develop their own lists and will not gatekeep new lists.

## Adding Your Token Logo

Syscoin token logos are [hosted here](https://github.com/pollum-io/tokens).
