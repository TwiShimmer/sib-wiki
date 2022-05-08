---
title: zh-cn.yml - 语言文件
description: 
published: true
date: 2022-05-08T00:58:07.317Z
tags: 
editor: markdown
dateCreated: 2022-05-08T00:58:07.317Z
---

## 自行修改
```yaml
prefix: "§7§l[§a经验泵§7§l]§r "

not_a_player: "§c操作失败: §7控制台无法进行此操作！"
invalid_param_amount: "§c操作失败: §7参数个数不正确！"
invalid_param_type: "§c操作失败: §7参数类型或数值不正确！"
invalid_pump: "§c操作失败: §7经验泵型号不存在！"
invalid_player: "§c操作失败: §7玩家不存在或不在线！"
no_permission: "§c操作失败: §7您没有权限！"
already_have: "§c操作失败: §7该玩家已经拥有该型号的经验泵！"
dont_have: "§c操作失败: §7该玩家没有该型号的经验泵！"
already_shared: "§c操作失败: §7该玩家已经在您的分享列表中！"
shared_limit: "§c操作失败: §7当前分享列表人数已经超过经验泵承载能力！"
shared_self: "§c操作失败: §7你不能给自己分享经验泵！"
successfully_share: "§a操作成功: §7已经将当前经验泵分享给该玩家{player}！"
successfully_shared: "§a注意: §7玩家{player}将经验泵分享给您！"
not_shared: "§c操作失败: §7该玩家本就不在您的分享列表中！"
successfully_delete: "§a注意: §7已经取消给玩家{player}的分享！"
successfully_give: "§a操作成功: §7给予玩家{player}新的经验泵{pump}！"
successfully_given: "§a注意: §7您收到了新的经验泵{pump}！"
successfully_remove: "§a操作成功: §7移除玩家{player}的经验泵{pump}！"
successfully_set: "§a操作成功: §7将玩家{player}的经验泵设置为{pump}！"
successfully_setted: "§a注意: §7您的经验泵型号被调整为{pump}！"
successfully_add: "§a操作成功: §7为玩家{player}添加经验泵运行时间{duration}秒！"
successfully_added: "§a注意: §7您的经验泵运行时间被添加{duration}秒！"

stop_working: "§7停止经验供给: §c经验泵能量不足！"
already_working: "§c操作失败: §7经验泵正在运行中，请等待本周期结束再尝试启动！"
cooldowning: "§c操作失败: §7经验泵正在冷却中 ({cd}秒)"
lack_of_materials: "§c材料不足: {material} §7× {amount}"
cant_multi_share: "§c操作失败: §7每个玩家同时最多享受一个经验泵输出！"

help:
  - "§aExpPump §7插件指令 §aMade By 南外丶仓鼠"
  - "§6★ §7 /ep help - §e查看指令帮助"
  - "§6★ §7 /ep menu [玩家] - §e打开经验泵菜单"
  - "§6★ §7 /ep addPump <型号> [玩家] - §e给予玩家对应型号的经验泵"
  - "§6★ §7 /ep delPump <型号> [玩家] - §e删除玩家对应型号的经验泵"
  - "§6★ §7 /ep setPump <型号> [玩家] - §e调整玩家当前经验泵的型号"
  - "§6★ §7 /ep addFuel <时间(秒)> [玩家] - §e增加玩家当前经验泵的时间"
  - "§6★ §7 /ep addShare <对象玩家> [玩家] - §e给一个玩家增加分享"
  - "§6★ §7 /ep delShare <对象玩家> [玩家] - §e给一个玩家取消分享"
  - "§6★ §7 /ep createFuel <ID> <数量> <名字> - §e添加手上的物品到材料库"
  - "§6★ §7 /ep deleteFuel <ID> - §e删除对应ID的材料"
  - "§6★ §7 /ep checkFuel - §e查看所有材料"
```