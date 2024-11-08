# EigenLayer AVS+Operator data from April to October 2024

## target files

`avs-tvl-by-day.json` shows AVS TVRs (total value of restaked assets), registered operators and shares (underlying restaked assets) for each day from 2024-04-10 to 2024-10-01.

`avs-metadata.json` and `operator-metadata.json` include the name and descriptions for each AVS and Operator. We can match across files using the `address` field for AVSs and Operators.

## source files

The following files have been extracted from the chain using an archive node.

1. `/operator-days` includes a series of files showing the delegated shares for each operator on each day. Fetched using the `getOperatorShares` method on the delegation contract (0x39053D51B77DC0d36036Fc1fCc8Cb819df8Ef37A).

2. `registration-events.json` includes a list of registration logs, describing the events in which an operator registered or de-registered for an AVS. Event `OperatorAVSRegistrationStatusUpdated` emitted by the address 0x135DDa560e946695d6f155dACaFC6f1F25C1F5AF.

## 3rd party data

The `/pricing` directory includes pricing data obtained from CoinGecko. This data has been used to calculate a USD denominated balance for restaked assets. Assets OETH and stETH have been priced as ETH (no significant depegs occurred during the period). Asset EIGEN has been priced at 0.

The information contained in the `-metadata.json` files has been collected by u--1 from the EigenLayer website.

## charts

The charts provide a visual aid to interpret data.

## testing

You can compare the latest entry in `avs-tvl-by-day.json` with the information on u--1.com and the EigenLayer website: https://app.eigenlayer.xyz/avs.

You can also use these historical snapshots of the u--1 website to compare AVS TVLs in the past:

21st May 2024: https://47e66fae.u--1.pages.dev/avs
30th June 2024: https://1b304224.u--1.pages.dev/avs

## author

u--1
@geeogi
