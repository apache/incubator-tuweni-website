---
layout: tutorial
title: Scraper
description: Scraper
group: nav-right
previous: index.md
categories: [applications]
---

Scraper is a discv5 server that constantly looks for new peers.

Whenever it connects to peers, it asks for all their known peers, and keeps going until it has exhausted all peers it could discover, then starts all over again.

Whenever a new peer is detected, its information is printed out to stdout with the following format:

<host address>,<udp port>,<attnets attribute>,<base-64 RLP encoding of the ENR>

The attnets attribute is an ENR attribute used by Ethereum 2.0.

Usage:

{%highlight bash%}
./scraper -LK4QC3FCb7-JTNRiWAezECk_QUJc9c2IkJA1-EAmqAA5wmdbPWsAeRpnMXKRJqOYG0TE99ycB1nOb9y26mjb_UoHS4Bh2F0dG5ldHOIAAAAAAAAAACEZXRoMpDnp11aAAAAAf__________gmlkgnY0gmlwhDMPYfCJc2VjcDI1NmsxoQOmDQryZJApMwIT-dQAbxjvxLbPzyKn9GFk5dqam4MDTYN0Y3CCIyiDdWRwgiMo
{%endhighlight%}