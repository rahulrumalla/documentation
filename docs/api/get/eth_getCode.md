# eth_getCode

## /v1/jsonrpc/:network/eth_getCode

Returns code at a given address.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_getCode?params=:paramsJSONArray`

#### HEADERS

`Content-Type: application/json`

#### REQUEST PARAMS
1. `ADDRESS` _[required]_ - a string representing the address (20 bytes) of the code
2. `BLOCK PARAMETER` _[required]_ - an integer block number, or the string "latest", "earliest" or "pending", see the [default block parameter](https://github.com/ethereum/wiki/wiki/JSON-RPC#the-default-block-parameter)

#### EXAMPLE
```bash
// GET
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_getCode?params=["0x06012c8cf97bead5deae237070f9587f8e7a266d","latest"]

// POST
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_getCode","params": ["0x06012c8cf97bead5deae237070f9587f8e7a266d"],"id":1}'
```

### RESPONSE

#### RESULT FIELDS
1. `CODE` - a hex of the code at the given address

#### BODY

```json
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x606060............"
}
```
