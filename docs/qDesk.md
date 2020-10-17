![Completion](https://img.shields.io/badge/completion-19%25-orange) ![Help Wanted](https://img.shields.io/badge/%20-help--wanted-%23159818) ![Version 0.9.3](https://img.shields.io/badge/stable-v0.9.4-green) ![Version 0.9.3](https://img.shields.io/badge/dev-v0.9.5-blue) ![Sponsors](https://img.shields.io/badge/sponsors-1-orange)

# qDesk
> Cross-Platform Trustless Social Network

![Screenshot](https://github.com/QuestNetwork/qd-messages-ts/raw/0.9.3/doc/images/0.9.3.png?raw=true)

>In case you are experiencing connectivity issues, on the app you can try using different [star node configurations](#troubleshooting) in Settings > IPFS.

# Description
qDesk is an example app for our JavaScript p2p library [Quest OS](quest-os-js) with cool open source modules like [qDesk Messages](qd-messages-ts) and [qDesk Social](qd-social-ts), as well as the upcoming [qDesk Markets](qd-market-ts), [qDesk News](qd-news-ts) and [qDesk Games](qd-games-ts).

We have chosen Angular/Electron as an example environment because we believe it offers the best accessibility for developers coming from any other language/framework. It is already being used in Python on PyQt5 and we aim to provide the underlying library in Go and wherever possible in Rust as well. 

qDesk makes it possible to build custom, secure and decentralized social networks in less than 20 days.

Our quest network aims to allow the creation and (distributed) completion of quests supported by a feature rich decentralized social network.

0.9.5+ allow to connect qDesk Social profiles to Twitter without sharing information with Twitter as an additional layer of verification. It is planned to add passive verification for a custom list of external networks to verify the peer identities.

1.0.0+ complies with privacy regulations and can be used for confidential information as a production social network for enterprises worldwide. 

This app is built on [Quest OS](quest-os-js) which makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/) and [IPFS DAGs](https://docs.ipfs.io/concepts/merkle-dag/).

Look what other people have built with qDesk: [Awesome Quest Network dApps](https://github.com/QuestNetwork/awesome/blob/master/README.md)!

qDesk allows to lazy load modules.

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
- [qDesk Messages \[Beta\]](qd-messages-ts)
- [qDesk Social \[Beta\]](quest-social-js)

**0.9.4**
- Encrypt Settings/Message History Files
- Change Swarm Peers In The Browser
- [Quest Network Coral Process](quest-coral-js)
- Additional Peering, option to pull from GitHub.
- Module Upgrades

# Roadmap

**0.9.5**
- [qDesk Games \[Beta\]](qd-games-ts) (for free items)
- [qDesk Apps \[Beta\]](qd-market-ts) (for free items)
- More Message Types And Inline Previews
- Native Audio/Video

**0.9.6**
- [qDesk Apps \[Beta\]](qd-apps-ts) (for paid items)
- [qDesk Games \[Beta\]](qd-games-ts) (for paid items)
- [qDesk Market \[Beta\]](qd-market-ts)
- Ethereum Payment Integration Beta

**0.9.7**
- [qDesk News \[Beta\]](qd-news-ts)
- Add Custom Themes By Pasting CSS Into The Built-In Theme Editor
- Import/Export Themes
- Light Mode
- Unlimited Custom Emojis

**0.9.8**
- Badges For Notifications
- Desktop Notifications

**0.9.9**
- Additional Patch
- [qDesk Vibes \[Beta\]](qd-vibes-ts) 

**1.0.0**
- [qDesk Quests \[Beta\]](qd-quest-ts)
- [qDesk Calendar \[Beta\]](qd-calendar-ts) personal & shared calendars. Add events from other modules on qDesk.
- [qDesk Messages \[Stable\]](qd-messages-ts)
- [qDesk Social \[Stable\]](quest-social-js)
- [qDesk Apps \[Stable\]](qd-apps-ts)
- Fork into [Vibenarium](https://github.com/Vibenarium/vibenarium-platform)
- Third Party Dependencies Audited, Security Issues Fixed
- Complies with global privacy laws

**2.0.0**
- [qDesk Calendar \[Stable\]](qd-calendar-ts)
- [qDesk Market \[Stable\]](qd-market-ts)
- [qDesk Vibes \[Stable\]](qd-vibes-ts) 
- Ethereum Payment Integration Finalized

**3.0.0**
- [qDesk Quests \[Stable\]](qd-quest-ts)
- [qDesk Games \[Stable\]](qd-games-ts)

**4.0.0**
- [OpenAI GPT3](https://en.wikipedia.org/wiki/GPT-3) Integration For Suggestions, AutoRespond And Completion

**5.0.0**
- Modular Crypto Currency Integration (presets for Bitcoin, Monero and Chainlink)


# Troubleshooting
**:warning: Messages are not being delivered || Participants won't update || Can't join channels**<br>
>Solution: qDesk ``^0.9.4`` go to ``Settings > IPFS`` and either download an example swarm peer list from GitHub (https://github.com/QuestNetwork/qDesk/blob/0.9.4/src/app/swarm.json) or enter your own.

If your problem is not solved here, please file an [issue](https://github.com/QuestNetwork/qDesk/issues/new) on GitHub.

