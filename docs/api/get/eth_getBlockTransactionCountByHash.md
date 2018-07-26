# /v1/jsonrpc/:network/eth_getBlockTransactionCountByHash

Returns the number of transactions in a block from a block matching the given block hash.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_getBlockTransactionCountByHash?params=:paramsJSONArray`

**HEADERS**

`Content-Type: application/json`

**REQUEST PARAMS**
1. `BLOCK HASH` _[required]_ - a string representing the hash (32 bytes) of a block

**EXAMPLE**
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_getBlockTransactionCountByHash?params=["0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35"]
```

### RESPONSE

**RESULT FIELDS**
1. `BLOCK TRANSACTION COUNT` - a hex code of the integer representing the number of transactions in the provided block 

**BODY**

```json
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x50"
}
```