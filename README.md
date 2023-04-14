# ensignJS
Welcome to ensignJS!

This repository contains the Ensign driver, SDK, and helpers for Javascript. For the main ensign repo, go [here](https://github.com/rotationalio/ensign). We also have SDKs for [Python](https://github.com/rotationalio/pyensign) and [Go](https://github.com/rotationalio/goensign).

## What's the best way to do streaming in JS?

Enabling convenient access to event streams is Ensign's core feature, but there are a few ways to expose streaming via JS and we're curious what you think would work best.

The options are below and the link to vote is [here](https://forms.gle/Jt3q18AbepqzjXxS7)!

### Option 1: WASM
This would be ideal because we could take the [Go code](https://github.com/rotationalio/go-ensign) and compile it for Javascript. But... will bidirectional streaming actually work? Has anyone tried this? Any suggestions?

### Option 2: gRPC-web
Solves the streaming in JS problem but only in the unidirectional case. Doesn't offer bidirectional streaming which is a pretty valuable Ensign feature. Also requires the Ensign core engineers to set up a proxy, and would have some additional implications for core Ensign development. But we can do that if you think that's the best choice...

### Option 3: Something custom
Appeal to the core Ensign engineers to create additional internal Ensign endpoints for HTTP 1 that can be used directly with the Fetch API. This would be more natural API queries and WebSockets but development might lag behind the core Ensign functionality. But maybe that's the best option? What do you think?