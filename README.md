# Bitford

A BitTorrent client as a Chrome Packaged App.

Contrary to other implementations, this one talks the native
BitTorrent protocol 100% in JavaScript.

**New:** install from the Chrome Web Store: https://chrome.google.com/webstore/detail/bitford/agjcpjkkccmhfopfciohkkfolnjbbdoh

## Try it

* Go to `chrome://extensions/`
* ☑ Developer mode
* Load unpacked extension...
* Choose this directory
* Launch
* Keep an eye on the console of the background page

## Roadmap

### UI

* Display file saving progress

### Background

* stealing by request age instead of timeouts
* seeder peers dropping
* Repair file saving
  * cancellable
  * no excess bytes
* Error handling
* store-backend: unify open bitford-store
* Tracker event
* Smarter request selection, based on downRate * requestedChunks.length
* Priorities & unchoke buckets, Tit-for-tat
* Peer connections should wait for store recovery progress
* Profiling, profiling, optimization

### Unsolved

* Intercept .torrent files that users download
  * https://github.com/Rob--W/pdf.js/commit/e181a3c902485a5c3e155c555abb6d686604457b

### Torrent Features

* Peer limits
  * by IP
  * Upload slots
* Extension protocol
* Magnet Links
* DHT
* Encryption
* uTP
