# Make Requests

### JSON-RPC Methods

Below is a quick command line example using CURL:

```
$ curl -X POST
-H "Content-Type: application/json"
--data '{"jsonrpc": "2.0", "id": 1, "method": "eth_blockNumber",
"params": []}'
"https://mainnet.infura.io/YOUR-API-KEY"
```

The result should look something like this:

```
$ {"jsonrpc": "2.0","result": "0x3ccb11", "id":1}
```

**NOTE:** "0x3ccb11" will be replaced with the block number of the most recent block on that network

[Read more about JSON RPC](https://github.com/ethereum/wiki/wiki/JSON-RPC)

Important to note that JSON-RPC is transport agnostic, meaning same concepts can be used over HTTP, sockets or other message passing environments. However, when using with Infura, there are endpoints are exclusive to 'socket' transports only (listed under the wss directory). 

### Rest-like Infura API

```
https://api.infura.io/v1/jsonrpc/mainnet/eth_blockNumber?token=YOUR-API-KEY
```
