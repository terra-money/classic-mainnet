# Terra Core & Columbus Launch
![banner](launch-banner.png)

This repository contains the configuration parameters for the Columbus Network Genesis. Columbus is the first decentralized network of nodes communicating over [Terra Core](https://github.com/terra-project/core). 

**_The Columbus mainnet will go live on April 23rd, 23:00 PST_** For participating validators, [the final genesis file](./genesis.json) is now up. Please bring up your nodes and get ready for launch!! 

## Important Notes for Validators

1. **For genesis Validators**: Please follow [these instructions](INSTRUCTIONS.md) to prepare for genesis, claim rewards from the drill, and get ready for genesis. 

2. **To stay updated for the genesis**: Please monitor the validator chat on Discord in real time to stay coordinated with Terraform Labs and the rest of the community regarding the launch. 

## Genesis Background

Terra is a project that is made possible thanks to the collective effort of its global community. Those of you interested in finding out the background of its genesis please see [here](./GENESIS.md) and our [blog](https://medium.com/terra-money). Final parameter settings for Columbus can be found [here](./params.README.md). 

## Terra community 

Community channels actively being moderated are here:
- [Website](https://terra.money/)
- [Discord](https://discord.gg/bYfyhUT)
- [Telegram](https://t.me/terra_announcements)
- [Twitter](https://twitter.com/terra_money)
- [YouTube](https://goo.gl/3G4T1z)

We will be making announcements regarding the launch using these channels, so please stay tuned. 

## Reference files

### Genesis files
 
- `penultimate_genesis.json`: The near-final genesis file, minus the gentx data validators must create and submit with this as the reference. 
- `/gentx`: Genesis transactions to create validators, submitted by each validator. 
- `/genesis.json`: The final genesis file that will be used to launch columbus.

### Seed Nodes

We request known community members who wish to run public p2p seed nodes make pull requests to add community run seed nodes below.

```
Known seed node list: 
b416f0b04e2c71b8d76f993468352030e2dcf2a9@public-seed-node.columbus.certus.one:26656  // certus
0621acccfc2c847e67d84eb234bcc26323a103c3@public-seed.terra.dev:26656  // terraform labs
46bba3a2c615ea5b569f086344f932fa11e81c01@public-seed2.terra.dev:26656 // terraform labs
6be0856f6365559fdc2e9e97a07d609f754632b0@terra-columbus-1-seed.nodes.polychainlabs.com:26656
7e221b46a861085eee8f59afdf28454a66e650db@159.69.112.67:26656 // syncnode
535222fdb795df6653934f22b8e5f16fdfacc9f6@seed.terra.de-light.io // de-light.io
```

```
Known peers:  
e6325ba7c490ba371135c9f3fcead66da1bd8cf1@terra-sentry01.dokia.cloud:26656
dba5defd7b120937da37aea7f37d06870637558d@terra-sentry02.dokia.cloud:26656
eb4ce12133c450ba6665e06309570ea2843e21d8@167.86.104.33:26656
7277be5ce17d60cf26c92a7cafbb9fc7da7f2be5@51.38.103.128:26656 // Castlenode
c7d4783415260b92d77b5fb74b1d86c6f4e69a1e@139.99.78.157:26656 // Figment 
1cb3e13efe7ca25fb68249169a15e85e53c3b3e9@terra-main.peer.nodeateam.kr:26656 // Node A-Team
46bc5183ef3b6ea9ffa84df16d6a5aa4a642427a@node.terra.forbole.com:26656 // Forbole
2df06e5217e73f27aede0ea0a9c1b8464ee5cf05@157.230.35.228:26656 // B-Harvest
```

## Disclaimer

The foundational software for the Columbus mainnet, Terra Core, is *highly* experimental software. In these early days, we can expect to have issues, updates, and bugs. The existing tools require advanced technical skills and involve risks which are outside of the control of Terraform Labs or its developers. Any use of this open source Apache 2.0 licensed software is done at your *own risk and on a “AS IS” basis, without warranties or conditions of any kind*. **Please exercise extreme caution!**



