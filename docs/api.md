quest-os-js


## async boot(config)

Boots the operating system. The GitHub branches master/0.9.2/0.9.3+ boot with:

JavaScript/NodeJS
```javascript
import { qOS } from '@questnetwork/quest-os-js'
// configure with a bootstrap swarm peer, for testing you can use:
let config = {
  ipfs: {
        Swarm: [<swarm star peer ip>,<swarm star peer ip>],
        quest-os-js: '',
        Gateway: ''
  },
  version: <version>
  dev: <true/false>
};
// boot the operating system
qOS.boot().then( () => {
  //the operating system is online, build the future
})
```

TypeScript/Angular Service
```javascript
import { Injectable } from '@angular/core';
import { qOS }  from '@questnetwork/quest-os-js';
import * as swarmJson from '../swarm.json';
import  packageJson from '../../../package.json';
const version = packageJson.version;

@Injectable({
  providedIn: 'root'
})
export class QuestOSService {
  public os;
  ready = false;
  config;
  constructor() {
    this.config = {
      ipfs: {
        Swarm: swarmJson['ipfs']['Swarm'],
        quest-os-js: '',
        Gateway: ''
      },
      version: version,
      dev: swarmJson['dev']
    };
    this.os = qOS;
  }
  async boot(){
      try{
        await this.os.boot(this.config);
        this.ready = true;
      }
      catch(e){
        throw(e);
      }
  }
}
```

## isReady()

Returns true once boot is complete, otherwise returns false.

```javascript
if(<os>.isReady()){
  console.log("Ready To Sign In");
};
```


## onReady()

Returns a Subject that pushes next when boot is complete

```javascript
if(<os>.onReady().subsribe( () => {
  console.log("Ready To Sign In");
});
```


## reboot()

Reboots the entire system

```javascript
<os>.reboot();
```

## enableSaveLock()
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Locks the system from saving any changes
```javascript
<os>.enableSaveLock();
```

## disableSaveLock()
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Unlocks the system from saving changes and saves changes normally
```javascript
<os>.disableSaveLock();
```


## setStorageLocation(location)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Sets the storage location for the app. Normally Quest OS does this automatically and you do not need to call this function.
Possible locations are: `"Download"`,`"LocalStorage"` or `"ConfigFile"`

```javascript
<os>.setStorageLocation("LocalStorage");
```

## getStorageLocation(location)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Returns a string with the current storage location

```javascript
<os>.getStorageLocation();
```


## setPwd(pwd)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Sets the password to be used with the next signIn attempt.

```javascript
<os>.setPwd(pwd);
```

## setPassword(old,new)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Sets the password to be used for encryption.
When you don't set this before sign in all data is encrypted with a random password.

```javascript
<os>.setPassword('','first-password');
```

## signIn(config = {})
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Activates Accounts. Empty config creates a new account
```javascript
<os>.signIn({});
```
## signOut()
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Deactivates Accounts And Restarts The Interface On The Web, Closes The Current Window In Electron
```javascript
<os>.signOut();
```

## onSignIn()
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Returns a subscribable Subject that fires when the account is signed in.
```javascript
<os>.onSignIn().subscribe( () => {
  console.log("Hello Universe");
});
```

## isSignedIn()
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js)

Returns a boolean true or false
```javascript
if(<os>.isSignedIn()){
  console.log("Hello Universe");
};
```

## channel

### async channel.create(dirtyChannelName, parentFolderId = "")
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns the clean channel name
```javascript
let claenChannelName = await <os>.channel.create('propaganda');
```

### channel.remove(cleanChannelName)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Removes a channel
```javascript
<os>.channel.remove('propaganda----1234');
```

### channel.listen(cleanChannelName)
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns a Subject that forwards non-system channel messages.
```javascript
<os>.channel.listen('propaganda----1234').subscribe( msg ){
  console.log(msg);
}
```

### async channel.publish(cleanChannelName, message, type = 'CHANNEL_MESSAGE')
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Returns a Subject that forwards non-system channel messages.
```javascript
await <os>.channel.publish('propaganda----1234',"Hello Universe");
```

## channel.challenge

### channel.challenge.enable(cleanChannelName)  
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Opens the channel to everyone who can solve the Captcha provided by [Quest Image Captcha JS](quest-image-captcha-js)
```javascript
<os>.channel.challenge.enable('propaganda----1234');
```

### channel.challenge.disable(cleanChannelName)
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Closes the channel to invite only participation
```javascript
<os>.channel.challenge.disable('propaganda----1234');
```

### channel.challenge.isEnabled(cleanChannelName)  
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

```javascript
if(<os>.isEnabled()){
  console.log("Hello Universe");
};
```

## channel.invite

### channel.invite.create(cleanChannelName,newInviteCodeMax, exportFolders = false)  
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Creates a new channel invite, specify max uses of this invite code and whether or not to include your folder structure.
```javascript
<os>.channel.invite.create('propaganda----1234',5,true);
```

### channel.invite.remove(cleanChannelName,link)
[![Bee](https://img.shields.io/badge/process-Bee-yellow)](quest-bee-js) [![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Removes a channel invite
```javascript
<os>.channel.invite.remove('propaganda----1234',"5448495320495320414e2045585452454d454c59204c4f4e4720414e4420494e56414c494420494e5649544520434f4445");
```

### channel.invite.get(channel)
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Gets all invites for a channel
```javascript
let invites = <os>.channel.invite.get('propaganda----1234');
```


### channel.invite.get(channel)
[![Ocean](https://img.shields.io/badge/process-Ocean-blue)](quest-ocean-js)

Gets all invites for a channel
```javascript
let invites = <os>.channel.invite.get('propaganda----1234');
```


**Unfortunately nobody is working on a detailed quest-os-js documentation yet, until then check out the source in [qDesk Messages](quest-messenger-js) 0.9.3+ to see how to use the OS.**

We recommend to use our [quest-cli](quest-cli) to test and build the package. It allows you to bootstrap your Quest Network apps with the same peers and settings.

Pro Tip: Put a file in your `/bin` that runs the quest-cli like so `node /path/to/quest-cli/index.js` from any folder on your system. It's much nicer!

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

