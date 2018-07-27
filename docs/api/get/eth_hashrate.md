# /v1/jsonrpc/:network/eth_hashrate

Returns the number of hashes per second that the node is mining with. Only applicable when the node is mining. 

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_hashrate`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_hashrate
```

### RESPONSE

#### RESULT FIELDS
1. `HASHRATE` - a hex code of an integer representing the number of hashes per second.

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x38a"
}
```
