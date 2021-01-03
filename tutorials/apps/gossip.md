---
layout: tutorial
title: Gossip
description: Gossip
group: nav-right
previous: index.md
categories: [applications]
---

The `gossip` application is an example showing how the Plumtree gossip implementation functions.

`gossip` is distributed as part of the binary distribution of Apache Tuweni, which you can download from this [page](/download)

{%highlight bash%}
./gossip --help
Usage: <main class> [-h] [--sending] [--numberOfMessages=<numberOfMessages>]
                    [--payloadSize=<payloadSize>]
                    [--sendInterval=<sendInterval>] [-c=<configPath>]
                    [-l=<port>] [-m=<messageLog>] [-n=<networkInterface>]
                    [-r=<rpcPort>] [-p[=<peers>...]]...
      --numberOfMessages=<numberOfMessages>
                            Number of messages to publish (load testing)
      --payloadSize=<payloadSize>
                            Size of the random payload to send to other peers (load
                              testing)
      --sending             Whether this peer sends random messages to all other
                              peers (load testing)
      --sendInterval=<sendInterval>
                            Interval to wait in between sending messages in
                              milliseconds (load testing)
  -c, --config=<configPath> Configuration file.
  -h, --help                Prints usage prompt
  -l, --listen=<port>       Port to listen on
  -m, --messageLog=<messageLog>
                            Log file where messages are stored
  -n, --networkInterface=<networkInterface>
                            Network interface to bind to
  -p, --peer[=<peers>...]   Static peers list
  -r, --rpc=<rpcPort>       RPC port to listen on
{%endhighlight%}

You can set up a `gossip` app to listen with this command:
{%highlight bash%}
./gossip -l 9000 -m /tmp/log
{%endhighlight%}

In a separate shell, you can send messages to the listener with:

{%highlight bash%}
./gossip -l 9001 -p 127.0.0.1:9000 --sending --payloadSize=32 --numberOfMessages=10 -p tcp://127.0.0.1:9000 --sendInterval=1000
{%endhighlight%}

This will send 10 messages, of 32 random bytes each. Open the file `/tmp/log` to see them.

You can create more complex scenarios with multiple gossip listeners, showing the path by which gossip circulates across peers.
