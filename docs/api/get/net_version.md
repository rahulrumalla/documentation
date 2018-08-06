# net_version

## /v1/jsonrpc/:network/net_version

Returns the current network id.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/net_version`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
// HTTP GET
curl https://api.infura.io/v1/jsonrpc/mainnet/net_version

// HTTP POST
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"net_version","params": [],"id":1}'
    
// WEBSOCKETS
>wscat -c wss://mainnet.infura.io/ws 
>{"jsonrpc":"2.0","method":"net_version","params": [],"id":1}
```

### RESPONSE

#### RESULT FIELDS
- `NETWORK ID` - a string representing the current network id.

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "1"
}
```
