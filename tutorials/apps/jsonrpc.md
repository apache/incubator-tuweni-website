---
layout: tutorial
title: JSON-RPC proxy
description: JSON-RPC proxy
group: nav-right
previous: index.md
categories: [applications]
---

The `jsonrpc` application is a JSON-RPC proxy that can cache, filter, throttle, meter and authenticate requests to a JSON-RPC endpoint.

The application is configured via a toml file, described below:

## Examples

### Proxy a JSON-RPC endpoint publicly

You set up a node and want to proxy. You expose all JSON-RPC methods on your node but only want to expose the `eth_` namespace publicly, with HTTP Basic authentication:

```toml
endpointUrl="http://192.168.1.2:8545" # IP of your node
allowedMethods=["eth_"]
cacheEnabled=true
cachedMethods=["eth_"]
cacheStoragePath="/var/jsonrpccache" # Cache location
```

### Local development

You have a local development and you're using a service such as Infura or Alchemy, but you want to work without calling the service constantly.

```toml
endpointUrl="https://example.com:8545/?token=mytoken" # service URL
cacheEnabled=true
cachedMethods=[""] # All methods are cached
cacheStoragePath="/var/jsonrpccache" # Cache location
allowedMethods=[""] # All methods are enabled
```

