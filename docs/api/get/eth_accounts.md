# /v1/jsonrpc/:network/eth_accounts

Returns a list of addresses owned by client.

### REQUEST

`GET https://api.infura.io/v1/jsonrpc/:network/eth_accounts`

#### HEADERS

`Content-Type: application/json`

#### EXAMPLE
```bash
curl https://api.infura.io/v1/jsonrpc/mainnet/eth_accounts
```

### RESPONSE

#### RESULT FIELDS
1. `ADDRESSES` - arrays of hex codes as strings representing the addresses owned by the client

#### BODY

```js
{
    jsonrpc: "2.0",
    id: 1,
    result: ["0xc94770007dda54cF92009BFF0dE90c06F603a09f"]
}
```
