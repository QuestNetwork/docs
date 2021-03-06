![Completion](https://img.shields.io/badge/completion-21%25-orange) ![Help Wanted](https://img.shields.io/badge/%20-help--wanted-%23159818) ![Version 0.9.3](https://img.shields.io/badge/stable-v0.9.4-green) ![Version 0.9.3](https://img.shields.io/badge/dev-v0.9.5-blue) ![Sponsors](https://img.shields.io/badge/sponsors-1-orange) [![Join the chat at https://gitter.im/QuestNetwork/qD](https://badges.gitter.im/QuestNetwork/qD.svg)](https://gitter.im/QuestNetwork/qD?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# qD

> Cross-Platform Trustless Social Network

![Screenshot](https://github.com/QuestNetwork/qd-messages-ts/raw/0.9.3/doc/images/0.9.3.png?raw=true)

>In case you are experiencing connectivity issues, on the app you can try using different [star node configurations](#troubleshooting) in Settings > IPFS.

# Description
qD is an example app for our JavaScript p2p library [qOS](quest-os-js) with cool open source modules such as [qD Messages](qd-messages-ts) and [qD Social](qd-social-ts) and the upcoming  [qD Vibes](qd-vibes-ts), [qD Markets](qd-market-ts), [qD News](qd-news-ts), [qD Apps](qd-apps-ts), [qD Games](qd-games-ts) and [qD Calendar](qd-calendar-ts).

qD makes it possible to build custom, secure and decentralized social networks in less than 20 days.

Our quest network aims to allow the creation and (distributed) completion of quests supported by a feature rich decentralized social network.

0.9.5+ allow to connect qD Social profiles to Twitter without sharing information with Twitter as an additional layer of verification. It is planned to add passive verification for a custom list of external networks to verify the peer identities.

1.0.0+ complies with privacy regulations and can be used for confidential information as a production social network worldwide.

We have chosen Angular/Electron as an example environment because we believe it offers the best accessibility for developers coming from any other language/framework. The Quest Network is already being used in Python on PyQt5 and we aim to provide the underlying library in Go and wherever possible in Rust as well.

This app is built on [qOS](quest-os-js) which makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/) and [IPFS DAGs](https://docs.ipfs.io/concepts/merkle-dag/).

Look what other people have built with qD: [Awesome Quest Network dApps](https://github.com/QuestNetwork/awesome/blob/master/README.md)!

qD allows to lazy load modules.

# Features

**0.9.3**
- Does not depend on the internet
- Does not depend on centralized servers
- No static external address or port forwarding necessary
- Dark Mode
- AutoSave For Settings
- Auto SignIn, if signed in
- Enhanced Mobile UI, Centered Snackbar, New Fonts, Icons & Buttons
- Included All Fonts And Icons In The Bundle
- Export Settings
- SignOut
- Enable Write Lock To Keep All Processes From Writing
- Disable AutoSave
- Change AutoSave Interval
- Dynamic Swarm Peer List On Desktop (add and remove bootstrap peers)
- App is now modular, makes building add-ons easy
- Drive Lock Fixed
- Offer "LocalStorage" As A Storage Container On The Web To Stay Signed In
- [qD Messages \[Beta\]](qd-messages-ts)
- [qD Social \[Beta\]](qd-social-js)

**0.9.4**
- Encrypt Account
- Change Swarm Peers In The Browser
- [Quest Coral Module](quest-coral-js)
- Additional Peering, option to pull from GitHub.
- Module Upgrades

**0.9.5**
- Account Name For Additional Security & Hashing
- qD redirects to the originally requested URI after signIn
- New Help Link

# Roadmap

**0.9.5**
- [Quest Quorum Module](quest-quorum-js)
- [qD Games \[Beta\]](qd-games-ts) (for free items)
- [qD Apps \[Beta\]](qd-apps-ts) (for free items)
- More Message Types And Inline Previews
- Native Audio/Video

**0.9.6**
- [qD Apps \[Beta\]](qd-apps-ts) (for paid items)
- [qD Games \[Beta\]](qd-games-ts) (for paid items)
- [qD Market \[Beta\]](qd-market-ts)
- Ethereum Payment Integration Beta

**0.9.7**
- [qD News \[Beta\]](qd-news-ts)
- Quest Worker To Render `.blend` Files And Earn Rewards
- Add Custom Themes By Pasting CSS Into The Built-In Theme Editor
- Import/Export Themes
- Light Mode
- Unlimited Custom Emojis

**0.9.8**
- Badges For Notifications
- Desktop Notifications

**0.9.9**
- Additional Patch
- [qD Vibes \[Beta\]](qd-vibes-ts)

**1.0.0**
- Polkadot Integration Beta
- [qD Quests \[Beta\]](qd-quest-ts)
- [qD Calendar \[Beta\]](qd-calendar-ts) personal & shared calendars. Add events from other modules on qD.
- [qD Messages \[Stable\]](qd-messages-ts)
- [qD Social \[Stable\]](qd-social-js)
- [qD Apps \[Stable\]](qd-apps-ts)
- Fork into [Vibenarium](https://github.com/Vibenarium/vibenarium-platform)
- Third Party Dependencies Audited, Security Issues Fixed
- Complies with global privacy laws

**2.0.0**
- [qD Calendar \[Stable\]](qd-calendar-ts)
- [qD Market \[Stable\]](qd-market-ts)
- [qD Vibes \[Stable\]](qd-vibes-ts)
- Ethereum Payment Integration Finalized

**3.0.0**
- [qD Quests \[Stable\]](qd-quest-ts)
- [qD Games \[Stable\]](qd-games-ts)
- Polkadot Integration Finalized

**4.0.0**
- [OpenAI GPT3](https://en.wikipedia.org/wiki/GPT-3) Integration For Suggestions, AutoRespond And Completion

**5.0.0**
- Modular Crypto Currency Integration (presets for Bitcoin, Monero and Chainlink)


# Troubleshooting
**:warning: Messages are not being delivered || Participants won't update || Can't join channels**<br>
>Solution: qD ``^0.9.4`` go to ``Settings > IPFS`` and either download an example swarm peer list from GitHub (https://github.com/QuestNetwork/qD/blob/0.9.4/src/app/swarm.json) or enter your own.

If your problem is not solved here, please file an [issue](https://github.com/QuestNetwork/qD/issues/new) on GitHub.

