# /v1/jsonrpc/:network/net_version

Returns the current network id.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/net_version`

**HEADERS**

`Content-Type: application/json`

**EXAMPLE**
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/net_version
```

### RESPONSE

**RESULT FIELDS**
1. `NETWORK ID` - a string representing the current network id.

**BODY**

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: "1"
}
```
