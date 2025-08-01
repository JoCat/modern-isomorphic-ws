# modern-isomorphic-ws

> [!NOTE]
> Starting with version 22.4.0, [Node.js includes a WebSocket](https://nodejs.org/docs/latest/api/globals.html#class-websocket) client API without an experimental flag.

Isomorphic WebSocket client implementation inspired by the [heinisuo/isomorphic-ws](https://github.com/heineiuo/isomorphic-ws) package.

It uses [ws](https://github.com/websockets/ws) on Node and native [WebSocket](https://developer.mozilla.org/en-US/docs/Web/API/WebSocket) in browsers.

## Limitations

Before using this module, you should be aware that ws is not fully compatible with the WebSocket API. It may not match the implementation in the browser, or it may introduce its own methods (for example, ping and pong, which are not in the browser version). You should always test your code in both Node and browsers for better compatibility and security.

## Difference from original isomorphic-ws

-   There is support for ES modules
-   Uses a shorter WebSocket export syntax in the browser, due to [almost 100% support](https://caniuse.com/mdn-api_websocket) for 2022 (for comparison, export in the [isomorphic-ws](https://github.com/heineiuo/isomorphic-ws/blob/0796a34cb4a5339ea39a4d335dcd9c6619c8b624/browser.js#L5-L15))

## Usage

You need to install both this package and [ws](https://github.com/websockets/ws):

`npm i modern-isomorphic-ws ws`

If you are using TypeScript, also set the type declarations:

`npm i @types/ws -D`

Now just import this package:

```ts
import WebSocket from "modern-isomorphic-ws";

// And write your code ;)
```
