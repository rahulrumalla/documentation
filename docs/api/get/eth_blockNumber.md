# /v1/jsonrpc/:network/eth_blockNumber

Returns the number of most recent block.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_blockNumber`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
// GET
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_blockNumber

// POST 
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params": [],"id":1}'
```

### RESPONSE

#### RESULT FIELDS
1. `BLOCK NUMBER` - a hex code of an integer representing the current block number the client is on.

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x5c174e"
}
```
