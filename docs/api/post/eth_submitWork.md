# eth_submitWork

## /v1/jsonrpc/:network/eth_submitWork

Used for submitting a proof-of-work solution.

### REQUEST

`POST https://api.infura.io/v1/jsonrpc/:network/eth_submitWork`

#### HEADERS

`Content-Type: application/json`

#### REQUEST PAYLOAD
1. `WORK ARRAY`
    - 8 Bytes - The nonce found (64 bits)
    - 32 Bytes - The header's pow-hash (256 bits)
    - 32 Bytes - The mix digest (256 bits)

#### EXAMPLE
```bash
// POST api.infura.io
curl https://api.infura.io/v1/jsonrpc/mainnet \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_submitWork","params": ["0x0000000000000001","0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef","0xD1FE5700000000000000000000000000D1FE5700000000000000000000000000"],"id":1}'

// POST mainnet.infura.io
curl https://mainnet.infura.io/ \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_submitWork","params": ["0x0000000000000001","0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef","0xD1FE5700000000000000000000000000D1FE5700000000000000000000000000"],"id":1}'
```

### RESPONSE

#### RESULT FIELDS
1. `IS VALID FLAG` - returns true if the provided solution is valid, otherwise false.

#### BODY

```json
{
  "id":1,
  "jsonrpc": "2.0",
  "result": false
}
```
