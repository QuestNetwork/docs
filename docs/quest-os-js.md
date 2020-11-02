![Completion](https://img.shields.io/badge/completion-14%25-orange) ![Help Wanted](https://img.shields.io/badge/%20-help--wanted-%23159818) ![Version 0.9.4](https://img.shields.io/badge/version-v0.9.4-green) ![Version 0.9.5](https://img.shields.io/badge/version-v0.9.5-blue) ![Sponsors](https://img.shields.io/badge/sponsors-0-red) [![Join the chat at https://gitter.im/QuestNetwork/qOS](https://badges.gitter.im/QuestNetwork/qOS.svg)](https://gitter.im/QuestNetwork/qOS?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# qOS

# Description
Unified API for the QuestNetwork dStack. Use with our example app: [qDesk](qDesk).

Main strategy is to create a Quest Network / IPFS / Ethereum interface that even kids can easily understand.

qOS offers encrypted channels, persistent storage, peer management, timelines, posts and more. It is used to load add-on modules, like [quest-coral-js](quest-coral-js) to use [IPFS DAGs](https://docs.ipfs.io/concepts/merkle-dag/), or [quest-dolphin-js](quest-dolphin-js) to use [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/).

# Installation & Usage
Check out our [API Reference](api.md) to get started!


``npm install @questnetwork/quest-os-js@0.9.4``

**OR**  

```
git clone quest-os-js && cd quest-os-js && git checkout 0.9.4 && cd ..
```

# Features

**0.9.2**
- Encrypted P2P Channels
- API for high level IPFS functionality
- Saves Config
- [Quest Ocean JS](quest-ocean-js)
- [Quest Bee JS](quest-bee-js)


**0.9.3**
- [Quest Social JS](quest-social-js)
- Documentation Extended
- Easier Access
- Offer "LocalStorage" As A Storage Container On The Web To Stay Signed In

**0.9.4**
- Change Peer Configuration in browser, Electron and on NodeJS
- Module Upgrades
- Password

**0.9.5**
- Account Name

# Roadmap

**0.9.5**
- [Quest Quorum Module](quest-quorum-js)
- Democratically block or mute peers
- Faux requests. Send request in channel, wait for response, deliver response as if it was an http request.

**0.9.6**
- Ethereum Payment Integration Beta

**0.9.7**
- Quest Worker To Render `.blend` Files And Earn Rewards
