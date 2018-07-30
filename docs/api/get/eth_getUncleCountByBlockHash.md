# eth_getUncleCountByBlockHash

## /v1/jsonrpc/:network/eth_getUncleCountByBlockHash

Returns the number of uncles in a block from a block matching the given block hash.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_getUncleCountByBlockHash?params=:paramsJSONArray`

#### HEADERS

`Content-Type: application/json`

#### REQUEST PARAMS
1. `BLOCK HASH` _[required]_ - a string representing the hash (32 bytes) of a block

#### EXAMPLE
```bash
// GET
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_getUncleCountByBlockHash?params=["0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35"]

// POST
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockHash","params": ["0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35"],"id":1}'
```

### RESPONSE

#### RESULT FIELDS
1. `BLOCK TRANSACTION COUNT` - a hex code of the integer representing the number of uncles in the provided block

#### BODY

```json
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x1"
}
```
