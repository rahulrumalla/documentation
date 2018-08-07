# Introduction
All examples in this reference secction will assume that the caller makes requests on the same sticky connection using web sockets. 

Some tools you can use for making these requests
- [WSCAT](https://github.com/websockets/wscat)
- [Advanced Rest Client](https://install.advancedrestclient.com/)

Important things to note when using Infura's WebSockets endpoint
- Invalid requests would result in a disconnect. 
- Idle connections will timeout after 1 hour.
- WebSockets have compression enabled by default.
- Maximum size of the the data/payload is 128MB.

#### EXAMPLE
The following is an example showing a connection to the WebSockets endpoint and using subscriptions through web3 
```js
const Web3 = require("web3");

const address = "0xb61f6e98898E2D13F1ARTGEc82567G389BBEB4";
const abi = [{abi code here}]

let web3 = new Web3(
  new Web3.providers.WebsocketProvider("wss://mainnet.infura.io/ws")
);

const instance = new web3.eth.Contract(abi, address);
instance.options.address = address;

instance.getPastEvents(
    "Adopted",
    { fromBlock: 0, toBlock: "latest" },
    (errors, events) => {
        if (!errors) {
            console.log("got events!");
            console.log(events.length);
        }
    }
);
```

