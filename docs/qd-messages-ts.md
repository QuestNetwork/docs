![Completion 1.0.0](https://img.shields.io/badge/completion%20v1.0.0-51%25-yellow) ![Help Wanted](https://img.shields.io/badge/%20-help--wanted-%23159818) ![Version 0.9.4](https://img.shields.io/badge/version-0.9.4-green) ![Version 0.9.5](https://img.shields.io/badge/version-0.9.5-blue) ![Sponsors](https://img.shields.io/badge/sponsors-1-orange)

# qD Messages

![Screenshot](https://github.com/QuestNetwork/qd-messages-ts/raw/0.9.3/doc/images/0.9.3.png?raw=true)

# Description

qDesk Messages is on track to become the first fully featured, cross-platform, publicly auditable, decentralized, real-time, dag based end-to-end encrypted messenger with a feature to exchange goods and services and send payments.

In this module you can create end-to-end encrypted channels, organize them in folders, share the folder structure with your invite, control the channels you own, participate in self-owned channels. Have private conversations or public channel discussions. Use Audio/Video in 0.9.5+ for groups or private conversations. Ban and report users in 0.9.5+. Alias and profile picture are linked from [qD Social](qd-social-ts). Peers can nickname participants and override the information that references other peers social profiles.

In 0.9.4 message histories are session only. In 0.9.5+ the message history is synced based on a quorum consensus scheme which creates an always online experience and lets peers view messages they missed when they were offline.

We are planning the integration of other messaging protocols like Matrix and IRC.

The messenger uses the second layer Quest Network PubSub protocol and if you are using [qOS](quest-os-js) in your application you can use the channels as well. This allows the use of bots. See the qOS API Reference for more information.

The messenger is a module for [qDesk](qDesk) and it's built on [qOS](quest-os-js) which makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/) and [qDesk](qDesk), our window platform based on [Angular10](https://angular.io/).

We have chosen Angular/Electron as an example environment because we believe it offers the best accessibility for developers coming from any other language/framework. The Quest Network is already being used in Python on PyQt5 and we aim to provide the underlying library in Go and wherever possible in Rust as well.

[qDesk](qDesk) works in the browser, as an Electron on Windows, Mac and Linux and Android using Cordova.

Check out other [Awesome Quest Network dApps](https://github.com/QuestNetwork/awesome/blob/master/README.md)!

# Features

**0.9.0**
- Does not depend on the internet
- Does not depend on centralized servers
- No static external address or port forwarding necessary
- Dark Mode
- Messages are signed using P-521 EC keypairs
- Encrypted P2P Channels (End-To-End, AES-256-CBC, Shared Via 4096 Bit OAEP)
- Organize Channels By Transport/Protocol And Custom Groups (like project folders in Atom)
- AutoSave For Settings
- [Quest Network PubSub Process](quest-pubsub-js)

**0.9.1**
- Auto SignIn, if signed in
- Create Channels/Folders
- Generate Invite Tokens (optional with folder structure)
- Import/Join From Invite Token (optional with folder structure)
- Delete Channels

**0.9.2**
- After 0.9.0 & 0.9.1 proved the concept, 0.9.2 is almost an entire rewrite
- IPFS Update (0.50.1)
- Enhanced Mobile UI, Centered Snackbar, New Fonts, Icons & Buttons
- Included All Fonts And Icons In The Bundle
- [Quest Network Operating System](quest-os-js)
- [Quest Network Bee Process](quest-bee-js)
- [Quest Network Ocean Process](quest-ocean-js)
- [Quest Network Dolphin Process](quest-dolphin-js)
- Delete Folders On Right Click
- Drag/Drop Folders/Channels
- Export Settings
- SignOut
- Enable Write Lock To Keep All Processes From Writing
- Disable AutoSave
- Change AutoSave Interval
- Disable Challenge Flow (close channels to invite only)
- Dynamic Swarm Peer List On Desktop (add and remove bootstrap peers)
- Share and Import Channels By QR Code

**0.9.3**
- [IPFS Update (0.50.2)](https://ipfs.io)
- App is now modular, makes building add-ons easy
- [qDesk Window Platform](https://qDesk.org)
- Drive Lock Fixed
- Offer "LocalStorage" As A Storage Container On The Web To Stay Signed In
- [qD Social](qd-social-ts)
- Combine messages sent in sequence
- Participant/Friends Folders
- Set Alias (show custom name instead of pub key) and profile pictures
- Private Encrypted P2P Channels (End-To-End, AES-256-CBC, Shared Via 4096 Bit OAEP)

**0.9.4**
- Scroll Bottom Fix
- Search for participants from [qD Social](qd-social-ts)
- Pair with participants by QR Code
- Click aliases to open stations.
- Online/Offline Status
- Improved Participant List
- Improved Favorites
- Encrypt Settings/Files
- [Quest Network Coral Process](quest-coral-js)
- Offline Participants are semi transparent and end of list

# Roadmap

**0.9.5**
- [qD Social](qd-social-ts) now allows to share private stations, so you can have direct conversations with people who have shared their private stations with you.
- Context Menu For Channels In Channel List
- Encrypted Audio/Video P2P Channels (Encryption Can Be Turned Off For Higher Quality)
- Encrypted Audio/Video Group Channels (Encryption Can Be Turned Off For Higher Quality)
- Ignore/Mute Channel Participants Locally
- Ban Channel Participants By Generating New Channel Names (ask representatives for new name, refuse banned participants
- Increase Security For Private P2P Channels
- Rename Channel/Favorite Folders
- Reactions (react to messages with emojis, GIFs and stickers)
- AutoSave And Quorum based P2P Sync For Message History Tree
- Export Message/Timeline Cache

**0.9.6**
- Ethereum Payment Integration Beta
- Channel Folders are now sorted alphabetically by default
- Sidebars resizable
- Magic Folder Explorer/Guide On Main (Delete Folders Also Called From Icon Click There)
- Parenting (reply to channel and private messages)
- Quote/Extend Messages (message inheritance)
- Encrypted P2P File Transfer (End-To-End AES-256-CBC, Shared Via 4096 Bit OAEP)
- AES Encrypt Invite Tokens
- Inline Preview For Media Files And Links (images, videos, etc)
- Magic Folders
- Stickers
- GIFs


**0.9.7**
- Private Channels Extendable To Groups (background create and join)
- Option to order channels by latest recent message
- Participant Status

**0.9.8**
- Banners For Channels And Channel Folders
- User Groups And Permissions
- Badges for unread messages
- Desktop Notifications

**1.0.0**
- Third Party Dependencies Audited, Security Issues Fixed
- Unlimited Custom Emojis
- Quest Network Calendar App Plugin (for shared calendars)
- IRC Plugin

**1.1.0**
- QuickResponse (from list of possible responses)
- AutoResponse (from quick responses)

**1.2.0**
- Tips & Guide That Explains The App In An Onscreen Overlay

**2.0.0**
- Ethereum Payment Integration Finalized

**3.0.0**
- Matrix Plugin to add Matrix rooms and communities

**4.0.0**
- [OpenAI GPT3](https://en.wikipedia.org/wiki/GPT-3) Integration For Suggestions, AutoRespond And Completion

**5.0.0**
- Quest Network Widgets (plug-in that connects the messenger to other apps, for example collaborative illustration in Inkscape)
- Modular Crypto Currency Integration (presets for Bitcoin, Monero and Chainlink)
- Share Screen
