---
title: 语言文件配置
description: 
published: true
date: 2022-06-29T07:05:11.623Z
tags: 
editor: markdown
dateCreated: 2022-06-29T07:05:11.623Z
---

本文主要简述NereusOpus默认配置中，涉及到语言配置的部分。
## 基础配置
```yaml
prefix: "§7§l[§a§lNereusOpus§7§l] "
celebrate_message: "§7恭喜玩家 §e{player} §7获得了附魔 {enchant}§7, 品质: {rarity}"
celebrate_title: "§e恭喜 {player}"
celebrate_subtitle: "§7获得了附魔 {enchant}§7, 品质: {rarity}"
```
## 异常反馈配置
```yaml
not_a_player: "§7操作失败: §c只有玩家才能使用该指令！"
invalid_param_amount: "§7操作失败: §c参数个数错误！"
invalid_param_type: "§7操作失败: §c参数必须是个整数！"
player_not_found: "§7操作失败: §c玩家不存在或不在线！"
enchant_not_found: "§7操作失败: §c附魔不存在或未被载入！"
rarity_not_found: "§7操作失败: §c品质不存在！"
type_not_found: "§7操作失败: §c类型不存在！"
no_permission: "§7操作失败: §c你没有权限！"
send_successfully: "§7操作成功: §a附魔书已经发至玩家背包（或掉落与脚下）！"
```
## 游戏内帮助
```yaml
help:
  - "§aNereusOpus §7插件指令: §aMade By 南外丶仓鼠"
  - "§6★ §7 /nereusopus help - §e查看指令帮助"
  - "§6★ §7 /nereusopus menu [玩家] - §e为玩家打开主菜单"
  - "§6★ §7 /nereusopus check [玩家] - §e为玩家打开附魔查询"
  - "§6★ §7 /nereusopus anvilCheck [玩家] - §e为玩家打开附魔铁砧试验台"
  - "§6★ §7 /nereusopus random [品质] [玩家] - §e给玩家一本随机的附魔书"
  - "§6★ §7 /nereusopus set <品质|类型> [玩家] - §e给玩家打开一个品质或类型的所有附魔的展示界面"
  - "§6★ §7 /nereusopus info <附魔> - §e查询一个附魔的基础信息"
  - "§6★ §7 /nereusopus query <附魔> [玩家] - §e查询一个附魔（界面）"
  - "§6★ §7 /nereusopus search <关键词> [玩家] - §e查找附魔（界面）"
  - "§6★ §7 /nereusopus mode <模式> [玩家] - §e打开特殊模式"
  - "§6★ §7 /nereusopus modify <附魔> <参数> <值> - §e设置附魔配置参数"
```

## 附魔信息存储与查阅格式
```yaml
info:
  - "§8| §7附魔名称: {displayname}"
  - "§8| §7附魔品质: {rarity}"
  - "§8| §7附魔介绍: {description}"

type:
  vanilla: "§b原版"
  curse: "§c诅咒"
  simple: "§a被动"
  skill: "§b主动"
  artifact: "§e粒子"

rarity_item:
  type: PLAYER_HEAD
  name: "{rarity}"
  lore:
    - "§8| 点击打开该类别的附魔大全界面"
type_item:
  type: PLAYER_HEAD
  name: "{type}"
  lore:
    - "§8| 点击打开该类别的附魔大全界面"
custom_item:
  type: ENCHANTED_BOOK
  name: "{displayname}"
  lore:
    - "§8| §7品质: {rarity}"
    - "§8| §7对象: §b{targets}"
    - "§8| §7等级: {level} / §c{maxlevel}级"
    - "§8| §7介绍: {description}"

conflict_item:
  type: ANVIL
  name: "§b附魔前置"
  denied_name: "§8| §7物品名: §e{denied_name}"
  denied_lore:
    start: "§8| §7物品描述: "
    contents: "    §7- {line}"
  denied_enchants:
    start: "§8| §7物品附魔: "
    contents: "    §7- {enchant} {roman}"
  non-conflict: "§8| §7无冲突"
  has-conflict: "§8| §7满足以上任一要求，即无法得到/打上该附魔（得到附魔书除外）"
```
## 附魔参数解读
> 此处可配置有关参数的具体翻译，便于玩家直接查阅。
{.is-info}
```yaml
enchant_params:
  amount: "数量/规模: §a{value}"
  chance: "触发几率: §a{value}%"
  repeat-ticks: "生效周期: §a{value}刻"
  durability-decrease: "耐久降低: §a{value}点"
  durability-increase: "耐久升高: §a{value}点"
  durability-decrease-extra: "额外磨损: §a{value}点"
  require-full-charge: "是否跟随攻击冷却: {value}"
  velocity: "加速度: §a{value}格/秒²"
  velocity-y: "垂直加速: §a{value}格/秒"
  velocity-xz: "水平加速: §a{value}格/秒"
  damage-multiplier: "伤害倍率: §a×{value}"
  damage-splash-multiplier: "溅射伤害: §a{value}%"
  damage-splash: "溅射伤害: §a{value}点"
  duration: "持续时间: §a{value}刻"
  amplifier: "效果等级: §a{value}级"
  disable-on-players: "是否对玩家生效: {value}"
  damage: "真实伤害: §a{value}点"
  power: "规模/力度: §a{value}"
  cause-fire: "是否引发火焰: {value}"
  break-blocks: "是否破坏方块: {value}"
  angle: "偏移角度: §a{value}°"
  decrease-if-cooldown: "是否存在冷却减幅: {value}"
  speed: "速度加成: §a{value}格/秒"
  range: "范围: §a{value}格"
  range-x: "x轴范围: §a{value}格"
  range-y: "y轴范围: §a{value}格"
  range-z: "z轴范围: §a{value}格"
  judge-range: "判定范围: §a{value}格"
  percent: "比例: §a{value}%"
  cooldown-decreased: "攻击冷却减幅: §a{value}%"
  min-health: "最低血量: §a{value}点"
  avaliable-on-players: "是否对玩家生效: {value}"
  drop-xp: "是否掉落经验: {value}"
  oxygen: "氧气值: §ga{value}点"
  min-distance: "最长生效距离: §a{value}格"
  max-health-increase: "最大血量增加: §a{value}点"
  drops: "掉落物: §a{value}"
  targets: "作用对象: §a{value}"
  exp-multiplier: "经验倍率: §a×{value}"
  heal: "回复血量: §a{value}点"

  colored: "是否附带发光颜色: {value}"

  sound: "释放音效: §a{value}"
  cooldown: "冷却时间: §a{value}秒"
  particle.type: "粒子效果: §a{value}"
  particle.amount: "粒子数量: §a{value}"
  permission-check: "是否检查方块权限: {value}"
  hardness-check: "是否检查方块硬度: {value}"
  disable-on-sneak: "是否在蹲下时禁用: {value}"
  enable-sound: "是否开启声音: {value}"
```
## PAPI变量与其它翻译
```yaml
true: "§a✔"
false: "§c✖"

papi_holders:
  player_level: "经验等级"
```