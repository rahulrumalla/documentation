# FAQ / FYI

**Endpoint?**

Infura's websocket endpoint : wss://`<network>`.infura.io/ws

**Support networks?**

Mainnet, Ropsten, Rinkeby, Kovan

**Batch Support?**

Yes

**Compression Enabled?**

Yes

**Max payload size?**

128MB

**Why does my websocket connection disconnect after a while?**

Idle connections that last more than an hour will get disconnected. Adding 'pings' to your websocket connection will prevent the connection from going idle.
Also, any unrecognized requests will trigger the server to close the connection with an error message.

**non-empty 'Sec-WebSocket-Protocol' header error?**

web3.js 1.0.0-beta.34 has an open issue with request headers https://github.com/ethereum/web3.js/issues/1559. Please revert/downgrade to 1.0.0-beta.33.


