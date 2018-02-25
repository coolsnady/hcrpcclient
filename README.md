hxrpcclient
============

[![ISC License](http://img.shields.io/badge/license-ISC-blue.svg)](http://copyfree.org)

hxrpcclient implements a Websocket-enabled hx JSON-RPC client package
written in [Go](http://golang.org/).  It provides a robust and easy to use
client for interfacing with a hx RPC server that uses a
hxd/bitcoin core-like compatible hx JSON-RPC API.

## Status

This package is currently under active development and in a beta state.
There are still several RPCs left to implement and the API is not stable yet.

## Documentation

* [hxd Websockets Example](https://github.com/hybridnetwork/hxrpcclient/blob/master/examples/dcrdwebsockets)  
  Connects to a hxd RPC server using TLS-secured websockets, registers for
  block connected and block disconnected notifications, and gets the current
  block count
* [hxwallet Websockets Example](https://github.com/hybridnetwork/hxrpcclient/blob/master/examples/dcrwalletwebsockets)  
  Connects to a hxwallet RPC server using TLS-secured websockets, registers for
  notifications about changes to account balances, and gets a list of unspent
  transaction outputs (utxos) the wallet can sign

## Major Features

* Supports Websockets (hxd/hxwallet) and HTTP POST mode (bitcoin core-like)
* Provides callback and registration functions for hxd/hxwallet notifications
* Supports hxd extensions
* Translates to and from higher-level and easier to use Go types
* Offers a synchronous (blocking) and asynchronous API
* When running in Websockets mode (the default):
  * Automatic reconnect handling (can be disabled)
  * Outstanding commands are automatically reissued
  * Registered notifications are automatically reregistered
  * Back-off support on reconnect attempts

## Installation

```bash
$ go get -u github.com/hybridnetwork/hxrpcclient
```

## License

Package hxrpcclient, like dcrrpcclient is licensed under the [copyfree](http://copyfree.org) ISC
License.
