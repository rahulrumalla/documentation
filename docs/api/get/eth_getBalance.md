# /v1/jsonrpc/:network/eth_getBalance

Returns the balance of the account of given address.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_getBalance?params=:paramsJSONArray`

**HEADERS**

`Content-Type: application/json`

**REQUEST PARAMS**
1. `ADDRESS` _[required]_ - a string representing the address (20 bytes) to check for balance
2. `BLOCK PARAMETER` _[required]_ - an integer block number, or the string "latest", "earliest" or "pending", see the [default block parameter](https://github.com/ethereum/wiki/wiki/JSON-RPC#the-default-block-parameter)

**EXAMPLE**
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_getBalance?params=["0xc94770007dda54cF92009BFF0dE90c06F603a09f","latest"]
```

### RESPONSE

**RESULT FIELDS**
1. `BALANCE` - integer of the current balance in wei.

**BODY**

```json
{
    jsonrpc: "2.0",
    id: 1,
    result: "0x29a33d8a9314006"
}
```