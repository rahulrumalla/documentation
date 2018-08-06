# eth_gasPrice

## /v1/jsonrpc/:network/eth_gasPrice

Returns the number of hashes per second that the node is mining with.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_gasPrice`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
// HTTP GET
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_gasPrice

// HTTP POST
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_gasPrice","params": [],"id":1}'
    
// SOCKETS
>wscat -c wss://mainnet.infura.io/ws 
>{"jsonrpc":"2.0","method":"eth_gasPrice","params":[],"id":73}
```

### RESPONSE

#### RESULT FIELDS
- `HASHRATE` - a hex code of an integer representing the current gas price in wei.

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x3b9acde7"
}
```
