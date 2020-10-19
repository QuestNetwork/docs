# Quest Quorum JS
> Core Module for the Quest Network Quorum Consensus.

# Description

The Quorum Core module for the [Quest Network Operating System](quest-os-js) interacts with [Quest Coral JS](quest-coral-js), [Quest Social JS](quest-social-js) and [Quest Dolphin JS](quest-dolphin-js) and can be loaded from [Quest OS](quest-os-js).

It synchronizes time and data resiliantly between peers. Uses elliptic curve cryptography in [Quest PubSub JS](quest-pubsub-js).

[Quest OS](quest-os-js) makes use of the [Interplanetary Filesystem](https://ipfs.io), [IPFS GossipSub](https://blog.ipfs.io/2020-05-20-gossipsub-v1.1/) and [IPFS DAGs](https://docs.ipfs.io/concepts/merkle-dag/).

When a peer quorum is used, Quest Quorum votes on a current time when assemblies are being created. It subsequently compares the responses and broadcasts of the participating peers.

**Default Consensus:**
In a valid assembly at least 71% of peers have to return the same result for the response to be accepted.

**Add-Ons:**
You can write add-ons for Quest Quorum that responses are piped through. There is an official [Quest Quorum Favorites](quest-quorum-fav-js) consensus scheme that is used by [qD Social](qd-social-ts) and [qD Messages](qd-messages-ts).

# Roadmap

**0.9.5**
- Basic functionality
