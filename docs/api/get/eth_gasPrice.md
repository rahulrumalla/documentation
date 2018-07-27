# /v1/jsonrpc/:network/eth_gasPrice

Returns the number of hashes per second that the node is mining with.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_gasPrice`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_gasPrice
```

### RESPONSE

#### RESULT FIELDS
1. `HASHRATE` - a hex code of an integer representing the current gas price in wei.

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x3b9acde7"
}
```
