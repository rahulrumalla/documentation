# /v1/jsonrpc/:network/eth_mining

Returns true if client is actively mining new blocks.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_mining`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_mining
```

### RESPONSE

#### RESULT FIELDS
1. `IS MINING FLAG` - a boolean indicating if the client is mining

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: true
}
```
