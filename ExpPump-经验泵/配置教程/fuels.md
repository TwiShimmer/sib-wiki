---
title: fuels.yml - 燃料库
description: 
published: true
date: 2022-05-08T00:55:48.422Z
tags: 
editor: markdown
dateCreated: 2022-05-08T00:29:50.611Z
---

## 见以下配置中的注释
```yaml
#燃料的内部ID，不可重复，可填写在config.yml经验泵的燃料列表中。
PX-1-A:
  #对应的物品，只有物品类型、名字、lore完全匹配的才可以判定为燃料
  item:
    #物品类型，见https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html
    type: DIAMOND_BLOCK
    #物品名，若没有则不填写这项
    name: 夏日冰熊
  #在经验泵控制面板中的名称
  name: 叫做『夏日冰熊』的钻石块
  #物品数量
  amount: 32
#可以自由添加，以下是其他默认燃料
PX-2-A:
  item:
    type: DIAMOND_BLOCK
  name: 钻石块
  amount: 32
PX-2-B:
  item:
    type: EMERALD_BLOCK
  name: 绿宝石块
  amount: 32
PX-3-A:
  item:
    type: DIAMOND_BLOCK
  name: 钻石块
  amount: 32
PX-3-B:
  item:
    type: EMERALD_BLOCK
  name: 绿宝石块
  amount: 32
PX-3-C:
  item:
    type: NETHERITE_BLOCK
  name: 下界合金块
  amount: 8
```
## 游戏内添加燃料
拿着需要添加的物品，输入/ep createFuel <内部ID> <数量> <显示名称>即可快速添加至燃料库。
举个例子，添加64个钻石作为一种燃料：
![燃料库3.png](/exppump/简介/燃料库3.png)
![燃料库2.png](/exppump/简介/燃料库2.png)

## 游戏内删除
输入/ep deleteFuel <内部ID>即可删除对应燃料
![燃料库4.png](/exppump/简介/燃料库4.png)

## 游戏内查看燃料库
输入/ep checkFuel即可查看所有燃料
![燃料库1.png](/exppump/简介/燃料库1.png)
