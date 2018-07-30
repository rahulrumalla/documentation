# net_peerCount

## /v1/jsonrpc/:network/net_peerCount

Returns the number of peers currently connected to the client.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/net_peerCount`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
// GET
curl https://api.infura.io/v1/jsonrpc/mainnet/net_peerCount

// POST
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"net_peerCount","params": [],"id":1}'
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
