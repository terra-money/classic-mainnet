# Terra Core & Columbus Launch

![banner](launch-banner.png)

This repository contains the configuration parameters for Columbus, Terra's official mainnet. Columbus is the first decentralized network of nodes communicating over [Terra Core](https://github.com/classic-terra/core).

To get a backgrounder on the network genesis, please refer [here](https://github.com/classic-terra/classic-mainnet/blob/master/GENESIS.md).

**[Columbus-5](https://github.com/classic-terra/classic-mainnet/tree/master/columbus-5) is the latest iteration of mainnet**.

## Terra community

Community channels actively being moderated are here:

- [Website](https://terrac.money)
- [Discord](https://discord.gg/P97BN33U)
- [Twitter](https://twitter.com/terrac_money)

We will be making announcements regarding network upgrades using these channels, so please stay tuned.

## Genesis

The genesis file for Columbus-5 is available [here](https://columbus-genesis.s3.ap-northeast-1.amazonaws.com/columbus-5-genesis.json)

## Seed Nodes

We request known community members who wish to run public p2p seed nodes make pull requests to add community run seed and peer nodes below.

```
Known seed node list:
e999fc20aa5b87c1acef8677cf495ad85061cfb9@seed.terra.delightlabs.io:26656
6d8e943c049a80c161a889cb5fcf3d184215023e@public-seed2.terra.dev:26656
87048bf71526fb92d73733ba3ddb79b7a83ca11e@public-seed.terra.dev:26656
3ddf51347ba7c2bc4a8e1e26ee9d1cbf81034516@162.55.244.250:27656
5618b310cfac1271a34f5c38576a5dceb1a641e6@162.55.132.48:15606
7cd549f6dab19000c260336c1a34479f8ff42964@54.154.91.139:26656
6ddd22cca53d2f0d03043614fc9f76acc72def8c@seed.terra-mainnet.everstake.one:26656
12e5d8f3602f63644cf548ffc83d886b5715a29f@kenaz.coinbevy.com:26656
ba5abb29421c44a8d5172d97206dd56342134a23@terra-mainnet-seed.larry.coffee:26656
65d86ab6024153286b823a3950e9055478effb04@terra.inotel.ro:26656
42928a07c8fe3313cfbfba78f296bf713e12a0a1@seed-columbus.terra.01node.com:26656
2b5ecb577e0fec2f15bc6c855dfe158f072a32a8@mnet-seed.terra.nitawa.systems:26656
235b5e97d7932e72fc846adcc712cd71e2a1b1be@seed.terra.lunarnode.org:26656
7575f4fdf92c4b63b2bf3e57ea0bced03b004792@3.35.101.38:26656
48fca58b12438e618a596e9aab634b4ef46ea67b@34.218.166.180:26656
1757b212d15840d9a8781bb4a8c201a9dd70d0fa@seed-mainnet.moonshot.army:26656
5e7cdd3f0684dbab8d7fa5d18de3e9194859be03@seed.terra.btcsecure.io:26656
b1bdf6249fb58b4c8284aff8a9c5b2804d822261@seed.terra.synergynodes.com:26656
92bcd725fb130530263704a4716da9c942becfa7@seed.mcontrol.ml:26656
cd0a58c2c9ee0613bf1988b3432fb2382f346a05@terra-mainnet-seed-1.stakin-nodes.com:26656
84a3a629a865245b94ac495f8c88e5717e4de9f1@terra-seed-server-01.stakely.io:26661
eb67380db62292506d41f28b1b77785a62a0f298@seed.terra.kkvalidator.com:26656
4f2d05162119a665b267599d3c86a936d65a9af0@seed.terra.rockx.com:26656
406bcf90a7b29df6ae475a1f94abe04ebde805af@mainnet.seed.terraindia.info:26656
1690a0c809314f2ff7f8e3ac559d5f30e7ba047b@65.108.9.149:26656
85963d3827ceab08be38285fbe354b90a2e45fef@seed-mainnet.terra.lunastations.online:36656
b977f4a6fe45b2621c2e009cdedc1d57c7f977ff@65.0.190.90:26656
ad2c60e2d9b5566385a192fac79ed540955266a4@194.163.167.27:26656
877c6b9f8fae610a4e886604399b33c0c7a985e2@terra.mainnet.seed.forbole.com:10056
```

```
Known peer list:
c545b9c4f3a902e505639c67a318b91b86e5060d@23.92.18.180:26656
adaf511ce1191db5673b1aa411d6765f99eb078d@172.104.133.249:26656
```

You can also download nightly address book by

```bash
curl https://raw.githubusercontent.com/classic-terra/classic-mainnet/master/columbus-5/addrbook.json > ~/.terra/config/addrbook.json
```

## Disclaimer

The foundational software for the Columbus mainnet, Terra Core, is *highly* experimental software. In these early days, we can expect to have issues, updates, and bugs. The existing tools require advanced technical skills and involve risks which are outside of the control of Terraform Labs or its developers. Any use of this open source Apache 2.0 licensed software is done at your _own risk and on a “AS IS” basis, without warranties or conditions of any kind_. **Please exercise extreme caution!**
