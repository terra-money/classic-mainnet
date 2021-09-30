# Terra Core & Columbus Launch

![banner](launch-banner.png)

This repository contains the configuration parameters for Columbus, Terra's official mainnet. Columbus is the first decentralized network of nodes communicating over [Terra Core](https://github.com/terra-money/core).

To get a backgrounder on the network genesis, please refer [here](https://github.com/terra-money/mainnet/blob/master/GENESIS.md).

**[Columbus-5](https://github.com/terra-money/mainnet/tree/master/columbus-5) is the latest iteration of mainnet**.

## Terra community

Community channels actively being moderated are here:

- [Website](https://terra.money/)
- [Discord](https://discord.gg/bYfyhUT)
- [Telegram](https://t.me/terra_announcements)
- [Twitter](https://twitter.com/terra_money)
- [YouTube](https://goo.gl/3G4T1z)

We will be making announcements regarding network upgrades using these channels, so please stay tuned.

## Genesis

The genesis file for Columbus-5 is available [here](https://columbus-genesis.s3.ap-northeast-1.amazonaws.com/columbus-5-genesis.json)

## Seed Nodes

We request known community members who wish to run public p2p seed nodes make pull requests to add community run seed nodes below.

```
Known seed node list:
e999fc20aa5b87c1acef8677cf495ad85061cfb9@seed.terra.delightlabs.io:26656
6d8e943c049a80c161a889cb5fcf3d184215023e@public-seed2.terra.dev:26656
87048bf71526fb92d73733ba3ddb79b7a83ca11e@public-seed.terra.dev:26656
```

You can also download nightly address book by

```bash
curl https://network.terra.dev/addrbook.json > ~/.terrad/config/addrbook.json
```

## Disclaimer

The foundational software for the Columbus mainnet, Terra Core, is *highly* experimental software. In these early days, we can expect to have issues, updates, and bugs. The existing tools require advanced technical skills and involve risks which are outside of the control of Terraform Labs or its developers. Any use of this open source Apache 2.0 licensed software is done at your _own risk and on a “AS IS” basis, without warranties or conditions of any kind_. **Please exercise extreme caution!**
