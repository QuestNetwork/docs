![Completion 1.0.0](https://img.shields.io/badge/completion%20v1.0.0-9%25-red) ![Help Wanted](https://img.shields.io/badge/%20-help--wanted-%23159818) ![Version 0.9.3](https://img.shields.io/badge/version-0.9.4-green) ![Version 0.9.3](https://img.shields.io/badge/version-v0.9.5-blue) ![Sponsors](https://img.shields.io/badge/sponsors-0-red)

# qD Social

# Description

qD Social offers the ability to share posts and information about yourself and make connections with other people. You can have a public profile, granular privacy settings or invite only. 

0.9.5+ allow to connect qD Social profiles to Twitter without sharing information with Twitter as an additional layer of verification. It is planned to add passive verification for a custom list of external networks to verify the peer identities.

1.0.0+ complies with privacy regulations and can be used for confidential information as a production social network for enterprises worldwide.

qD Social is a module for [qDesk](qDesk). It's accessible across qDesk, you can use it with [qD Messages](qd-messages-ts) and other qDesk modules. It is used to show store information and latest store campaigns on [qD Market](qd-market-ts). 

qD Social is built on [Quest OS](quest-os-js) which makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/), [IPFS DAGs](https://docs.ipfs.io/concepts/merkle-dag/), and [qDesk](qDesk), our example app based on [Angular10](https://angular.io/).

[qDesk](qDesk) works in the browser, as an Electron on Windows, Mac and Linux and Android using Cordova and makes it possible to build custom, secure and decentralized social networks in less than 20 days.

We have chosen Angular/Electron as an example environment because we believe it offers the best accessibility for developers coming from any other language/framework. The Quest Network is already being used in Python on PyQt5 and we aim to provide the underlying library in Go and wherever possible in Rust as well.

Use [Quest OS](quest-os-js) in your applications and you can use the underlying channels and data in your own application by booting with [Quest Social JS](quest-social-js).

Check out other [Awesome Quest Network dApps](https://github.com/QuestNetwork/awesome/blob/master/README.md)!

# Features

**0.9.3**
- Public Profile
- Invite Only Profile
- Alias, Full Name, About

**0.9.4**
- Pair by QR Code
- Search For Social Profiles Received From All Connected Modules
- Native Posts
- Profile & Timeline Search
- Comments/Replies On Posts
- Favorite List
- Improved Timeline Propagation 
- Replies modularized
- Uses IPFS merkle-trees now

# Roadmap

**0.9.5**
- Report Posts & Users
- Ban Users
- Share Private Profiles 
- Custom Timeline Search Algorithms
- Native Followers
- Connect To Twitter

**0.9.6**
- Use up To 5 Social Profiles Simultaneously 
- Change Profile Picture
- Change Poster
- Connect [Markets](qd-market-ts)
- Connect To Other Platforms (write custom adapters, with our requests you can also inlcude centralized platforms by our twitter example)


**1.0.0**
- Connect [Vibenarium](https://github.com/Vibenarium/vibenarium-platform)
