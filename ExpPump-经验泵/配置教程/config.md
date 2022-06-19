---
title: config.yml-总设置
description: 
published: true
date: 2022-06-19T08:17:00.248Z
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
#是否允许玩家同时接受多个物质泵的分享，或是一边开自己的物质泵，一边获得其他玩家的分享
allowMultiShare: true
#可变的指令 例如默认配置生效时，玩家输入/pump和/ep会有同样的效果
alias:
  - ep
  - pump
#额外加成特权，可以分配给VIP
#可以自由添加与删除，格式：'权限:加成倍率'
#例如默认配置生效时，玩家拥有exppump.extra.25，则其物质泵总输出提升25%
#拥有多个权限不叠加，仅取最大的加成计算
extras:
  - "exppump.extra.25:0.25"
  - "exppump.extra.50:0.50"
  - "exppump.extra.75:0.75"
  - "exppump.extra.100:1.0"
#启用物质泵的玩家头顶的粒子效果
particle:
  #是否启用这个功能
  enable: true
  #粒子效果的类型，见https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Particle.html
  type: TOTEM
  #粒子效果的数量，不宜过多
  amount: 5
#GUI界面对物质泵剩余时间的显示（秒）
left:
  #满状态（绿色）
  full: 5400
  #充足状态（蓝色）
  enough: 3600
  #不足状态（黄色）
  some: 1800
  #枯竭状态（橙色）
  little: 0
#所有物质泵的设置
#你可以自己添加，复制粘贴改改即可，请注意ID不要重复（不要出现两个PX-1或是其他相同ID）
pumps:
  #ID
  PX-1:
    #物质泵的名称
    name: "PX-1经验泵"
    #物质泵的类别（EXP代表经验，MONEY代表游戏币，POINT代表点券，CMD代表执行指令）
    type: EXP
    #物质泵每秒钟输出多少（EXP、MONEY、POINT），或表示物质泵每多少秒执行一次指令（CMD）
    speed: 4
    #最大分享人数
    maxShare: 2
    #最大续航时间（超过本时间时再添加燃料无效）
    maxDuration: 7200
    #每分享给一个人，总输出增加多少（这里是+15%）
    increase: 0.15
    #可用的燃料
    fuels:
      - A
  PX-2:
    name: "PX-2游戏币泵"
    type: MONEY
    speed: 10
    maxShare: 0
    maxDuration: 7200
    increase: 0
    fuels:
      - B
  PX-3:
    name: "PX-3点券泵"
    type: POINT
    speed: 1
    maxShare: 0
    maxDuration: 7200
    increase: 0
    fuels:
      - C
  PX-4:
    name: "PX-4废话泵"
    type: CMD
    duration: 10
    cmds:
      - "msg {%}player} 每十秒说一句话"
    maxShare: 0
    maxDuration: 7200
    increase: 0
    fuels:
      - D