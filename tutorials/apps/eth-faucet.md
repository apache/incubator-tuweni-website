---
layout: tutorial
title: Ethereum Faucet
description: Ethereum Faucet
group: nav-right
previous: index.md
categories: [applications]
---

The `eth-faucet` application is an Ethereum faucet that runs alongside an Ethereum client. The faucet allows to distribute funds.

The faucet works with a configuration file, `application.yml`. Here is a template of the file:

{%highlight yaml%}
server:
  use-forward-headers: true
  forward-headers-strategy: native
spring:
  main:
    banner-mode: "off"
  security:
    oauth2:
      client:
        registration:
          github:
            clientId: <your github client ID>
            clientSecret: <your github client secret>
html:
  title: Faucet
  request_message: Welcome to our faucet. You can ask for up to 1 ETH on this faucet.

security:
  oauth2:
    client:
      preEstablishedRedirectUri: <registered github redirect URI>
      registeredRedirectUri: <registered github redirect URI>
      useCurrentUri: false

faucet:
  maxETH: <the maximum amount of eth, in ETH, that you>
  chainId: <chain id of your network>
  rpcPort: <Ethereum client RPC port>
  rpcHost: <Ethereum client RPC host>

wallet:
  path: wallet.key
banner: >
  Apache Tuweni Faucet example.

           `:oyhdhhhhhhyo-`
         :yds/.        ./sdy:
       :mh:                :hm:
     `ym:                    :my`
     hm`                      `mh
    +N.                        .N+
    my :ydh/              /hdy- ym
    Mo`MMMMM`            .MMMMN oM
    my /hdh/              +hdh: ym
    +N.                        .N+
     hm`              `m:     `mh
     `ym:    `sssssssssN:    :my`
       :dh:   ``````````   :hd:
         :yds/.        ./sdy:
           `-oyhdhhhhdhyo-`
{%endhighlight%}

You should register a Github OAuth application to go along and fill the template.