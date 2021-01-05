---
layout: tutorial
title: Hobbits Relayer
description: Hobbits Relayer
group: nav-right
previous: index.md
categories: [applications]
---

The `hobbits-relayer` application showcases how to use the Hobbits protocol to pass messages between different networks.

{%highlight bash%}
hobbits-relayer --help
Usage: <main class> [-h] [-b=<bind>] [-t=<to>]
  -b, --bind=<bind>   Endpoint to bind to
  -h, --help          Prints usage prompt
  -t, --to=<to>       Endpoint to relay to
{%endhighlight%}

Example use:

Relay messages over TCP from port 21000 to 22000:
{%highlight bash%}
hobbits-relayer -b tcp://localhost:21000 -t tcp://localhost:22000
{%endhighlight%}

Relay messages over UDP from port 2222 to 4444:
{%highlight bash%}
hobbits-relayer -b udp://localhost:2222 -t udp://localhost:4444
{%endhighlight%}

Relay messages from a Web Socket port 2222 to a TCP server on 4444:
{%highlight bash%}
hobbits-relayer -b ws://localhost:2222 -t tcp://localhost:4444
{%endhighlight%}


