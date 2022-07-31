---
title: config.yml 总配置文件
description: 
published: true
date: 2022-07-31T05:16:42.700Z
tags: 
editor: markdown
dateCreated: 2022-07-31T00:49:15.704Z
---

```yaml
#插件序列码
cdkey: "序列码"

#验证库信息，**勿改**
captcha:
  ip: "XXXXXXXXXXXXX"
  port: XXXXX

#语言文件
language: zh_cn.yml

#是否可突破原来的最高等级（强化上限在下方设置）
override-maxLevel: true
#是否可突破原版冲突
override-vanilla-conflicts: true
#是否可以突破原版物品类型判定
override-vanilla-targets: false
#是否可以突破 NereusOpus 提供的一系列限制（如附魔种类上限）
override-nereusopus: false

#强化上限（未设置则默认为原版最高级）
maxLevel:
  #格式为“附魔: 最高等级”
  #
  锋利: 1000
  #可继续添加

#反噬惩罚
failed-punishment:
  #破碎：失去对应强化装备
  break:
    enable: false
  #降级（在破碎为false时生效）
  decrease:
    enable: true
    #降多少级（random表示0-1的随机小数，计算后取整）
    level: 1+9*random

#强化成功的公告
broadcast-if-success:
  #bossbar信息
  broadcast:
    #是否启用
    enable: true
    #能触发boss信息的最低强化等级，maxLevel表示强化上限
    min-level: 0.01*maxLevel
    text: "§7恭喜玩家 §e%player% §7成功强化装备附魔: §8%enchant% %old-roman% §7→ §b%enchant% %new-roman%"
  bossbar:
    enable: true
    min-level: 0.1*maxLevel
    text: "§7恭喜玩家 §e%player% §7成功强化装备附魔: §8%enchant% %old-roman% §7→ §b%enchant% %new-roman%"

#额外消耗货币
extra-expense:
  #游戏币（需要Vault插件）
  vault:
    #是否启用
    enable: true
    #消耗公式，currentLevel表示强化前等级，maxLevel表情强化上限，intensifyLevel表示强化多少级
    amount: 10000*(currentLevel/maxLevel)*intensifyLevel
  #点券（需要Playerpoints插件）
  playerpoints:
    #是否启用
    enable: false
    amount: 100*(currentLevel/maxLevel)*intensifyLevel
  #经验等级
  exp-level:
    #是否启用
    enable: false
    amount: 30*(currentLevel/maxLevel)*intensifyLevel

#DNF机制：附魔越多强化越难
dnf:
  #成功率额外降低
  success-rate:
    #是否启用
    enable: true
    #降低成功率公式，currentLevel表示强化前等级，maxLevel表情强化上限
    amount: 20*(currentLevel/maxLevel)
  #反噬率额外升高
  fail-rate:
    #是否启用
    enable: false
    #升高反噬率公式，currentLevel表示强化前等级，maxLevel表情强化上限
    amount: 20*(currentLevel/maxLevel)

#特权
#添加格式：
# "权限|表达式"
#表达式格式：
#sr:<数字> 成功率添加多少
#fr:<数字> 反噬率降低多少
privileges:
  - "enchantintensifier.sr.5|sr:5"
  - "enchantintensifier.sr.10|sr:10"
  - "enchantintensifier.fr.5|fr:5"
  - "enchantintensifier.fr.10|fr:10"
```