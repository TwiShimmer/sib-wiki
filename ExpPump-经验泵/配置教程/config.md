---
title: config.yml-总设置
description: 
published: true
date: 2022-06-19T05:40:53.900Z
tags: 
editor: markdown
dateCreated: 2022-05-08T00:32:49.542Z
---

## config.yml
```yaml
#插件数据存储所在的文件夹（绝对路径，DefaultFolder代替插件默认配置文件夹）
statFolder: "DefaultFolder/stats/"
#使用的语言
language: "zh-cn.yml"
#数据存储周期（秒），不建议设置过短
savePeriods: 1200
#是否允许玩家同时接受多个经验泵的分享，或是一边开自己的经验泵，一边获得其他玩家的分享
allowMultiShare: true
#可变的指令 例如默认配置生效时，玩家输入/pump和/ep会有同样的效果
alias:
  - 经验泵
  - 经验
  - ep
  - pump
#额外加成特权，可以分配给VIP
#可以自由添加与删除，格式：'权限:加成倍率'
#例如默认配置生效时，玩家拥有exppump.extra.25，则其经验泵总输出提升25%
#拥有多个权限不叠加，仅取最大的加成计算
extras:
  - "exppump.extra.25:0.25"
  - "exppump.extra.50:0.50"
  - "exppump.extra.75:0.75"
  - "exppump.extra.100:1.0"
#启用经验泵的玩家头顶的粒子效果
particle:
  #是否启用这个功能
  enable: true
  #粒子效果的类型，见https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Particle.html
  type: TOTEM
  #粒子效果的数量，不宜过多
  amount: 5
#所有经验泵的设置
#你可以自己添加，复制粘贴改改即可，请注意ID不要重复（不要出现两个PX-1或是其他相同ID）
pumps:
  #默认的PX-1
  PX-1:
    #经验泵的名称
    name: "PX-1型经验泵"
    #经验泵每秒钟输出多少点经验（总输出）
    speed: 4
    #经验泵最多分享给多少玩家
    maxShare: 2
    #每多分享给一位玩家，经验泵总输出增加多少（默认是15%）
    increase: 0.15
    #经验泵禁用的燃料，除了这个燃料，燃料库里其他燃料都可以用于启动经验泵
    deniedFuels:
      - "PX-1-A"
  PX-2:
    name: "PX-2型经验泵"
    speed: 8
    maxShare: 4
    increase: 0.2
    deniedFuels: []
  PX-3:
    name: "PX-3型经验泵"
    speed: 12
    maxShare: 8
    increase: 0.25
    deniedFuels: []