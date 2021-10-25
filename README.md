# Twine Protocol

Twine Protocol is a simple way to exchange payloads between two running processes.

See the [wiki](https://github.com/teleclimber/twine-protocol/wiki/The-Twine-Protocol) where I dump some thoughts and current info.

The implementations can work using different transports:

- Unix sockets
- WebScokets
- WebRTC (maybe? Haven't tried to implement yet)
- postMessage?

## Use Cases

- A front end and a back end
- A sandboxed process and its host
- ...

## Why?

I wanted a simple way to communicate between two processes without reinventing a message protocol every time. More:

- Simple and effective. Lightweight.
- Reasonably performant. Small messages. Minimal handshake.
- Quick to adopt: no code-gen. Just import and use.
- Reusable in different environments (transports) to I don't have to learn a new thing.
- Payload-agnostic. Send JSON, strings, binary data, or just a single byte.
- Bidirectional. Either side can send.
- Powerful enough to support non-trivial exchange of information that might occur between two running functions.

## Implementations

- [twine-web](https://github.com/teleclimber/twine-web) 
- [twine-go](https://github.com/teleclimber/twine-go)
- [twine-deno](https://github.com/teleclimber/twine-deno)

## State of Development

It's extremely early. I'm dogfooding this in Dropserver and learning as I go. Implementations leave a lot to be desired.

There is more in the Wiki here on Github.
