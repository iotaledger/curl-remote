# Sandbox - IOTA.js Library Shim

This library is used to shim the [iota.lib.js](https://github.com/iotaledger/iota.lib.js) library to allow for it to be used with the Sandbox. This enables for users to offload PoW from web user or small devices without capabilities. 

This library has been constructed for [this sandbox application](#). 

## Basic Usage

The library exposes one function, which your require or import. This function is used to overlay sandbox functionality to your current `iota.lib.js` instance.

```javascript
// Import the Sanbox Monkey Patch for the IOTA lib
const sandboxPatch = require('sandbox.lib.js')

// Patch the current IOTA instance
sandboxPatch(iota, `https://sandbox.testnet.iota.org`, 500, `sdkd...sdaa`)
```

1. **iota**: `Object` The `iota.lib.js` instance in your application
2. **url**: `String` URL of the sandbox you wish to use
3. **delay**: `Integer` Milliseconds to wait before checking for PoW update. *Null value defaults to 1000*
4. **key**: `String` API key used to raise the un-authenticated API limits. *Optional*

## API Key

In order to receive an API you should go to the following URL to receive an API for the IOTA Testnet: 

```bash
https://sandbox.testnet.iota.org
```



If you are running your own sandbox, please generate a token from the appropriate sources