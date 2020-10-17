![Completion 1.0.0](https://img.shields.io/badge/completion%20v1.0.0-0%25-red) ![Help Wanted](https://img.shields.io/badge/%20-help--wanted-%23159818) ![Version 0.9.3](https://img.shields.io/badge/version-v0.9.5-blue) ![Sponsors](https://img.shields.io/badge/sponsors-0-red)

# qDesk Apps

# Description

qDesk Apps is a module for [qDesk](https://qDesk.org). It's accessible across qDesk, you can use it with qDesk Messages, qDesk Social and other qDesk modules. This module allows peers on the network to exchange, discuss, categorize and rate apps democratically.

Use [Quest OS](https://github.com/QuestNetwork/quest-os-js) in your applications and you can use the underlying channels and data in your own application by booting with [Quest News JS](https://github.com/QuestNetwork/quest-news-js).

qDesk Apps allows users to share apps hosted on the [Interplanetary Filesystem](https://ipfs.io). Starting with our last patch for the rewrite 0.9.9+ premium app licenses can be purchased with Ethereum. qDesk Apps is a module for [qDesk](https://github.com/QuestNetwork/qDesk) and it's built on [Quest OS](https://github.com/QuestNetwork/quest-os-js) which makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/) and [qDesk](https://github.com/QuestNetwork/qDesk), our example app based on [Angular10](https://angular.io/).

We have chosen Angular/Electron as an example environment because we believe it offers the best accessibility for developers coming from any other language/framework. It is already being used in Python on PyQt5 and we aim to provide the underlying library in Go and wherever possible in Rust as well.

[qDesk](https://github.com/QuestNetwork/qDesk) works in the browser, as an Electron on Windows, Mac and Linux and Android using Cordova.

Check out other [Awesome Quest Network dApps](https://github.com/QuestNetwork/awesome/blob/master/README.md)!

# Commands

**Prepare Package**

``npm run inst`` Removes `package-lock.json` and runs ``npm install``

We added an example ```swarm.json``` to the ```src/app``` folder with an example node to make reproduction easier, but we strongly recommend to use our [Quest CLI](https://github.com/QuestNetwork/quest-cli) to test and build the app.

Pro Tip: Put a file in your `/bin` that runs the quest-cli like so `node /path/to/quest-cli/index.js` from any folder on your system. It's much nicer!

# Features

**0.9.5**
- Basic functionality
