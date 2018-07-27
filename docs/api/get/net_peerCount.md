# /v1/jsonrpc/:network/net_peerCount

Returns the number of peers currently connected to the client.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/net_peerCount`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/net_peerCount
```

### RESPONSE

#### RESULT FIELDS
1. `PEER COUNT` - integer of the number of connected peers.

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x64"
}
```
