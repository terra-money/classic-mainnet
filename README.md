# Terra Core & Columbus Launch
![banner](launch-banner.png)

This repository contains the configuration parameters for the Columbus Network Genesis. Columbus is the first decentralized network of nodes communicating over [Terra Core](https://github.com/terra-project/core). 

To get a backgrounder on the network genesis, please refer [here](https://github.com/terra-project/launch/blob/master/GENESIS.md).

**[Columbus-3](https://github.com/terra-project/launch/tree/master/columbus-3) has now launched**

## Terra community 

Community channels actively being moderated are here:
- [Website](https://terra.money/)
- [Discord](https://discord.gg/bYfyhUT)
- [Telegram](https://t.me/terra_announcements)
- [Twitter](https://twitter.com/terra_money)
- [YouTube](https://goo.gl/3G4T1z)

We will be making announcements regarding network upgrades using these channels, so please stay tuned. 

## Genesis
Download the columbus-3 genesis [Here](https://columbus-genesis.s3-ap-northeast-1.amazonaws.com/genesis.json)

## Seed Nodes

We request known community members who wish to run public p2p seed nodes make pull requests to add community run seed nodes below.

```
Known seed node list: 
US Region:
6be0856f6365559fdc2e9e97a07d609f754632b0@terra-columbus-3-seed.nodes.polychainlabs.com:26656  // Polychain
925ecc3de9e2ac65a203beb2333ced1a00c135ed@terra-seed-us.chorus.one:28657 // Chorus One (US)

Asia Region:
87048bf71526fb92d73733ba3ddb79b7a83ca11e@public-seed.terra.dev:26656  // Terraform Labs
b5205baf1d52b6f91afb0da7d7b33dcebc71755f@public-seed2.terra.dev:26656 // Terraform Labs
5d9b8ac70000bd4ab1de3ccaf85eb43f8e315146@seed.terra.delightlabs.io:26656 // DELIGHT LABS

Europe Region:
bae08cc880c20aeda68a5a890a71a9b44ac73cb4@terra-seed-eu.chorus.one:28657 // Chorus One (EU)

Not reachable at the moment:
// 447ba60df6fdc2466e1ab4c328e100d6bc5765f8@seed-only.terra-columbus-3.bas.network:26656 // BasBlock
// b416f0b04e2c71b8d76f993468352030e2dcf2a9@public-seed-node.columbus.certus.one:26656  // certus
```

You can also download nightly address book by
```bash
curl https://network.terra.dev/addrbook.json > ~/.terrad/config/addrbook.json
```

## Disclaimer

The foundational software for the Columbus mainnet, Terra Core, is *highly* experimental software. In these early days, we can expect to have issues, updates, and bugs. The existing tools require advanced technical skills and involve risks which are outside of the control of Terraform Labs or its developers. Any use of this open source Apache 2.0 licensed software is done at your *own risk and on a “AS IS” basis, without warranties or conditions of any kind*. **Please exercise extreme caution!**



