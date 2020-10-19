
# bee

## comb

### bee.comb.get(path)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Gets HoneyComb Object Or Array Of Objects.

```javascript
let comb = <os>.bee.comb.get('/my/path/to/the/object');
```

### bee.comb.set(path,content)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Sets HoneyComb Object Or Array Of Objects.

```javascript
<os>.bee.comb.set('/my/path/to/the/object',content);
```

### bee.comb.add(path,content)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Adds a HoneyComb object to an array of HoneyComb objects.

```javascript
<os>.bee.comb.add('/my/path/to/the/object',content);
```

### bee.comb.search(path)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Searches for HoneyComb objects and returns a flat array of HoneyComb objects.

```javascript
let results = <os>.bee.comb.search('/my/path');
```
# coral

## dag

### async set(path, unencrytpedObject,storagePath)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns the reference object.

``
let latestRef = <os>.ocean.coral.dag.set('/my/path',unencrytpedObject,{ storagePath: '/archive/social/timeline/transaction' });
``

### async add(path, unencrytpedObject,storagePath)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns the reference object.

``
let latestRef = <os>.ocean.coral.dag.add('/my/path',unencrytpedObject,{ storagePath: '/archive/social/timeline/transaction' });
``

### async get(pathOrCid, config = {})
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)


Returns the decrypted object or array of objects.
``
let array = <os>.ocean.coral.dag.get('/my/path',{ limit: 5 });
``
# crypto

## aes

### generatePassphrase(length)

Returns a new secure AES passphrase.
```javascript
let pwd = <os>.crypto.aes.generatePassphrase(length);
```

### hashSecret(message,newSecret, rounds = 10)

Hashes a secret for the specified amount of rounds, anything below 5000 rounds will default to 5000.
```javascript
let hashed = <os>.crypto.aes.hashSecret(message,newSecret, rounds = 10);
```

### encrypt(utf8OrObject, whistle = undefined)

Encrypts an object or utf8 string either with the whistle supplied or with a generated new whistle.
Returns Base64.
```javascript
let { secret, aesEncryptedB64 } = <os>.crypto.aes.encrypt('test');
```

### decryptB64(aesEncryptedB64, secret, format = 'utf8')

Decrypts a B64 string with the whistle
Returns String or Object.
```javascript
let { secret, aesEncryptedB64 } = <os>.crypto.aes.decryptB64(aesEncryptedB64, secret, format = 'utf8')
```

### decryptHex(enc,secret, format = 'utf8'

Decrypts a Hex string with the whistle
Returns String or Object.
```javascript
let { secret, aesEncryptedB64 } = <os>.crypto.aes.decryptHex(aesEncryptedHex, secret, format = 'utf8')
```

## convert

### stringToArrayBuffer(string,format)

Returns an ArrayBuffer of the input string.
```javascript
let aB = <os>.crypto.convert.stringToArrayBuffer(string,'utf8');
```

### bufferToArrayBuffer(buf)

Returns an ArrayBuffer of the input butter
```javascript
let hashed = <os>.crypto.convert.bufferToArrayBuffer(buf);
```

### async importKey(alg,format,keyenc,key)

Imports a key for WebCrypto.
```javascript
await <os>.crypto.convert.importKey(alg,format,keyenc,key);
```

## ec

### async digest(algo,data)

Digests data using the supplied algorithm.
```javascript
let digest = await <os>.crypto.ec.digest('SHA-256',data);
```

### async generateKeyPair()

Generates an EC keypair with maximum security according to the Quest Network protocol.
```javascript
let keys = await <os>.crypto.ec.generateKeyPair();
```

### async sign(obj, keyHex)
Signs an object with an EC private Hex key according to the Quest Network protocol.
```javascript
let signedObject = await <os>.crypto.ec.sign(obj,keyHex);
```

### verify(obj, keyHex)
Verifies a signed object with an EC public Hex key according to the Quest Network protocol.
```javascript
if(await <os>.crypto.ec.verify(obj,keyHex)){
  console.log('Signature Checks Out!');
}
```

## rsa

### async generateKeyPair()

Generates an RSA keypair with maximum security according to the Quest Network protocol.
```javascript
let keys = await <os>.crypto.rsa.generateKeyPair();
```

### async fullEncrypt(plain,pubKey)

Encrypts a string with an RSA private key
```javascript
let encrypted = await <os>.crypto.rsa.fullEncrypt(plain,pubKey);
```


### async fullDecrypt(enc,pk)
Decrypts a string with an RSA public key
```javascript
let decrypted = await <os>.crypto.rsa.fullDecrypt(encrypted,pk);
```

# dolphin

## async sayHi(channel)

Send the sayHi message in a given channel.

```javascript
await <os>.ocean.dolphin.sayHi(channel)
```
# social

## profile

### social.profile.togglePrivacy(profilePubKey = 'NoProfileSelected')
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Toggles your profile's visibility between private and public, not giving a pubKey will automatically select your first profile.
In private mode you have to manually share your profile with everyone you want to see your details. In Public mode all the members of the channels you're in can see your profile.

```javascript
<os>.social.profile.togglePrivacy();
```

### social.profile.isPublic(socialPubKey = 'NoProfileSelected')
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Checks if a profile has public visibility, not giving a pubKey will automatically select your first profile.

```javascript
if(<os>.social.profile.isPublic(socialPubKey)){
  console.log("Hello Universe");
};
```

### social.profile.isFavorite(socialPubKey)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Checks if a profile is in our favorites, returns boolean true or false.

```javascript
if(<os>.social.profile.isFavorite(socialPubKey)){
  console.log("Hello Universe");
};
```

### social.profile.isRequestedFavorite(socialPubKey)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Checks if a profile is a requested favorite, returns boolean true or false.

```javascript
if(<os>.social.profile.isRequestedFavorite(socialPubKey)){
  console.log("Hello Universe");
};
```

### social.profile.search(searchPhrase)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)  

Will automatically search for all social profiles in the peers network where alias, full name or about text match the phrase.
This version of the methos is case sensitive by default, future versions will allow a config object.

Returns an array with the search results and adds the following fields:
```
isFavorite: boolean
isRequestedFavorite: boolean
```

```
let results = <os>.social.search('Bob');
```

## timeline


### async social.timeline.getReferenceTree(socialPubKey)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns an array with the unresolved timeline of the requested peer.

```javascript
let timeline = await <os>.social.timeline.get(socialPubKey)){
};
```


### async social.timeline.get(socialPubKey)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns an array with the resolved timeline of the requested peer.

```javascript
let timeline = await <os>.social.timeline.get(socialPubKey)){
```

## post

### social.timeline.post.delete(qHash)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Deletes a post by its qHash.

```javascript
async <os>.social.timeline.post.delete(qHash);
```

### async social.timeline.post.new(postObj = { content: '', socialPubKey:'' })
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Creates a new post on the timeline of the owner of the socialPubKey.

```javascript
<os>.social.timeline.post.new(postObj = { content: '', socialPubKey:'' })
```

### propagate(latestRef, postObj)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Propagates the latest timeline ref across channels.

```javascript
async <os>.social.timeline.post.propagate(latestRef, postObj)
```


## agent

### async social.timeline.agent.sync(pubKey = "all", config = { limit: 5,  storagePath: '/archive/social/timeline/transaction' })
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Syncs the timeline for a given pubkey or all cached pubkeys.

```javascript
async <os>.social.timeline.agent.sync(pubKey);
```

### async social.timeline.agent.groupTimeline(timeline,  limit = 0)
[![Social](https://img.shields.io/badge/process-Social-green)](quest-social-js) [![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Creates a new post on the timeline of the owner of the socialPubKey.

```javascript
<os>.social.timeline.agent.groupTimeline(timeline,  limit = 0)
```

