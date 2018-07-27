# /v1/jsonrpc/:network/web3_clientVersion

Returns the current client version.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/web3_clientVersion`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/web3_clientVersion
```

### RESPONSE

#### RESULT FIELDS
1. `STRING` - The current client version

#### BODY

```json
{
    jsonrpc: "2.0",
    id: 1,
    result: "Geth/v1.8.6-patched-leveldb-8818ab0b/linux-amd64/go1.9.2"
}
```
