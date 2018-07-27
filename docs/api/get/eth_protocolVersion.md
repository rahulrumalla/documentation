# /v1/jsonrpc/:network/eth_protocolVersion

Returns the current ethereum protocol version.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_protocolVersion`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_protocolVersion
```

### RESPONSE

#### RESULT FIELDS
1. `PROTOCOL VERSION` - a string indicating the current ethereum protocol version

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "54""
}
```
