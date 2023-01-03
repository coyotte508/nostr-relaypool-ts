# nostr-relaypool-ts
A Nostr RelayPool implementation in TypeScript using only nostr-tools library as a dependency 

Install:
npm i nostr-relaypool

Usage:

```
let relays = ["wss://relay.damus.io", "wss://nostr.fmt.wiz.biz", "wss://nostr.bongbong.com"];
let relaypool = new RelayPool(relays)
let sub=relayPool.sub([{authors: '32e1827635450ebb3c5a7d12c1f8e7b2b514439ac10a67eef3d9fd9c5c68e245'}], relays)
sub.onevent((event)=>console.log(event))
sub.oneose((events, url)=>{console.log(events, url)})  // Called for each relay
```
