---
title: Config.yml
description: 
published: true
date: 2022-05-08T00:33:51.362Z
tags: 
editor: markdown
dateCreated: 2022-05-08T00:32:49.542Z
---

```statFolder: "DefaultFolder/stats/"

language: "zh-cn.yml"

defaultPump: "PX-1"

savePeriods: 1200

allowMultiShare: true

alias:
  - 经验泵
  - 经验
  - ep
  - pump

extras:
  - "exppump.extra.25:0.25"
  - "exppump.extra.50:0.50"
  - "exppump.extra.75:0.75"
  - "exppump.extra.100:1.0"

particle:
  enable: true
  type: TOTEM
  amount: 5

pumps:
  PX-1:
    name: "PX-1型经验泵"
    duration: 7200
    speed: 4
    maxShare: 2
    increase: 0.15
    fuels:
      - "PX-1-A"
    cd: 3600
  PX-2:
    name: "PX-2型经验泵"
    duration: 14400
    speed: 8
    maxShare: 4
    increase: 0.2
    fuels:
      - "PX-2-A"
      - "PX-2-B"
    cd: 7200
  PX-3:
    name: "PX-3型经验泵"
    duration: 28800
    speed: 12
    maxShare: 8
    increase: 0.25
    fuels:
      - "PX-3-A"
      - "PX-3-B"
      - "PX-3-C"
    cd: 14400```