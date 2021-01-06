---
layout: tutorial
title: Tuweni Application
description: Tuweni Application
group: nav-right
previous: index.md
categories: [applications]
---

The `tuweni` application is an Ethereum client that can run multiple chains and multiple discovery mechanisms.

`tuweni` can sync multiple chains at once. It also has a web UI.

NOTE: everything at this point is at best a prototype. This may change at any time.

Usage:

{%highlight bash %}
Apache Tuweni client loading
Usage: <main class> [-h] [-c=<configPath>] [-w=<web>]
  -c, --config=<configPath>
                    Configuration file.
  -h, --help        Prints usage prompt
  -w, --web=<web>   Web console host:port
{%endhighlight%}

Most of the action happens in the configuration file, written with TOML.

Example with one chain:

{%highlight toml %}
[storage.default]
path="data"
genesis="default"
[genesis.default]
path=default.json
{%endhighlight%}

The `default.json` file is your usual genesis configuration file.

Example with two chains:

Example with one chain:

{%highlight toml %}
[storage.foo]
path="data"
genesis="foo"
[genesis.foo]
path=default.json
[storage.bar]
path="data"
genesis="bar"
[genesis.bar]
path=other.json
{%endhighlight%}
