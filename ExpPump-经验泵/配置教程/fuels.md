---
title: fuels.yml-燃料库
description: 
published: true
date: 2022-06-19T05:43:00.732Z
tags: 
editor: markdown
dateCreated: 2022-05-08T00:29:50.611Z
---

## fuels.yml
```yaml
#燃料的内部ID，不可重复，可填写在config.yml经验泵的燃料列表中。
钻石块:
  #对应的物品，只有物品类型、名字、lore完全匹配的才可以判定为燃料
  item:
    #物品类型，见https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html
    type: DIAMOND_BLOCK
    #物品名，若没有则不填写这项
    name: 夏日冰熊
    #物品lore，若没有则不填写这项
    lore: wakuwaku
  #在经验泵控制面板中的名称
  name: 叫做『夏日冰熊』的钻石块
  #一个燃料可以启动经验泵的时间(秒)
  duration: 3600
#可以自由添加，以下是其他默认燃料
```
## 游戏内添加燃料
拿着需要添加的物品，输入/ep createFuel <内部ID> <显示名称> <时间>即可快速添加至燃料库。

## 游戏内删除
输入/ep deleteFuel <内部ID>即可删除对应燃料

## 游戏内查看燃料库
输入/ep checkFuel即可查看所有燃料
