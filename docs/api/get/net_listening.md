# /v1/jsonrpc/:network/net_listening

Returns true if client is actively listening for network connections.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/net_listening`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/net_listening
```

### RESPONSE

#### RESULT FIELDS
1. `LISTENING FLAG` - a boolean indicating whether the client is actively listening for network connections

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: true
}
```
