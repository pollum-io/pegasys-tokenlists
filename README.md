# Pegasys Tokenlists

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow the specification. The Pegasys community invites you to add your token to our tokenlists!

## Adding Your Token to an Existing List
### General Requirements
To integrate your token into the Pegasys app you must submit a PR following these steps:

1. Token should be verified on the [block explorer](https://explorer.syscoin.org/).
2. Tokens are added to tokenlists by Pegasys team based on market demand and other metrics. 

3. Make sure to let us know of your interest through our [Discord channel](https://discord.gg/kAq3pAUAkE) by reaching out to anyone from our team over at the `Support -> 🌱│new-tokens` channel.
4. Fork the Github repository, preferably to your team's Github organization.
5. Create a new folder with the [_checksum formatted_](https://piyolab.github.io/sushiether/RunScrapboxCode/?web3=1.0.0-beta.33&code=https://scrapbox.io/api/code/sushiether/web3.js_-_Ethereum_のアドレスをチェックサム付きアドレスに変換する/demo.js) smart contract address of your token inside logos(mixed case `0xa5B6...` address).
6. Tell your designer that token image must be in PNG format, preferably transparent background, recommended size 256x256px, with max file size of 100kB.
7. Upload your logo with file named `logo.png` to previously created folder, i.e. `logos/0x0000000000000000000000000000000000000bAe/logo.png`
8. Add an entry in the `tokens` field of the appropriate tokenlist. Here is an example:
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
9. Update the `timestamp` field to the current timestamp.
10. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.

## Creating Your Own List

List creation is encouraged! The Pegasys team wants the community to develop their own lists and will not gatekeep new lists.
## Have more questions?
Come visit us on discord at our `dev-talk` channel. 
Link: https://discord.gg/kAq3pAUAkE

## Disclaimer
Pegasys team allows anyone to submit new assets to this repository. However, this does not mean that we are in direct partnership with all of the projects.

The Pegasys team will reject projects that are deemed as scam or fraudulent after careful review. We also reserve the right to change the terms of asset submissions at any time due to changing market conditions, risk of fraud, or any other factors we deem relevant. We hold no responsibility to add your token under any circumstances.
