# /v1/jsonrpc/:network/eth_getWork

Returns the hash of the current block, the seedHash, and the boundary condition to be met ("target").

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_getWork`

**HEADERS**

`Content-Type: application/json`

**EXAMPLE**
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_getWork
```

### RESPONSE

**RESULT FIELDS**
1. `WORK ARRAYS`
    - 32 Bytes - current block header pow-hash
    - 32 Bytes - the seed hash used for the DAG.
    - 32 Bytes - the boundary condition ("target"), 2^256 / difficulty.


**BODY**

```js
{
  "id":1,
  "jsonrpc":"2.0",
  "result": [
      "0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef",
      "0x5EED00000000000000000000000000005EED0000000000000000000000000000",
      "0xd1ff1c01710000000000000000000000d1ff1c01710000000000000000000000"
    ]
}
```
