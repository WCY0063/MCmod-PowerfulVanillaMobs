# 更强大的原版生物 (Powerful Vanilla Mobs)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Minecraft](https://img.shields.io/badge/Minecraft-1.21.1-blue)](https://www.minecraft.net)
[![NeoForge](https://img.shields.io/badge/NeoForge-21.1.226-red)](https://neoforged.net)

> 让原版生物脱胎换骨 —— 三个强大 Boss / 友方单位，各自拥有独特的技能、双形态与奖励系统。

---

## 内容

| 单位 | 类型 | 生命 | 描述 |
|---|---|---|---|
| **幻翼之王·奈特梅尔** | Boss | 1024 | 三阶段巨型幻翼，远程火球 + 法阵 + 召唤 + 终极技能 |
| **无敌的白铁之星** | 友方 | 500 | 高频近战 + 瞬移 + 多重免疫，仇恨所有敌对生物 |
| **绿袍尊者** | 友方 | 800 | 远程施法者，9 种技能（翠玉弹、荆棘之鞭、生命汲取……），受击瞬移 |

## 特性

- 🎯 **三种生成方式**：刷怪蛋 / `/summon` 指令 / 自然条件生成
- 🩸 **阶段系统**：奈特梅尔根据血量切换行为，血条颜色同步变化
- 🌙 **双形态**：奈特梅尔在主世界白天或异维度强化，冷却缩短 40%
- 💬 **全服公告**：Boss 出场 / 战败均有酷炫聊天提示
- 🎁 **战利品箱**：奈特梅尔死亡掉落含传说武器"奈特梅尔之牙"
- 🃏 **自然变异**：傻子村民有 1% 概率突变为绿袍尊者
- 📊 **累计召唤**：击杀 100 只幻翼后奈特梅尔自动降临

## 快速开始

### 前置

- **Minecraft 1.21.1**
- **NeoForge 21.1.226+**
- **Java 21**

### 安装

1. 从 [Releases](https://github.com/YOUR_USERNAME/PowerfulVanillaMobs/releases) 下载 `PowerfulVanillaMobs.jar`
2. 放入 `.minecraft/mods/` 目录
3. 启动游戏

### 生成方式

| 实体 | 获取 |
|---|---|
| 奈特梅尔 | 刷怪蛋 / `/summon giant_phantom_boss:giant_phantom_boss` / 杀 100 幻翼 |
| 白铁之星 | 刷怪蛋 / `/summon giant_phantom_boss:white_iron_golem` |
| 绿袍尊者 | 刷怪蛋 / `/summon giant_phantom_boss:jade_sage` / 傻子村民 1% 变异 |

## 构建

```bash
# 生成 Gradle wrapper（首次）
gradle wrapper

# 构建
./gradlew build
# Windows: gradlew.bat build

# 输出: build/libs/PowerfulVanillaMobs.jar
```

## 项目结构

```
src/main/java/com/giantphantomboss/
├── GiantPhantomBoss.java          # 模组主入口
├── PhantomKillTracker.java        # 事件处理（公告/击杀计数/变异/战利品）
├── entity/
│   ├── GiantPhantomBossEntity.java # 幻翼之王
│   ├── WhiteIronGolemEntity.java   # 白铁之星
│   └── JadeSageEntity.java         # 绿袍尊者
├── init/
│   ├── ModEntities.java            # 实体类型注册
│   └── ModItems.java              # 刷怪蛋注册
└── client/
    ├── ClientEvents.java           # 客户端渲染器注册
    └── renderer/                   # 实体渲染器
```

## 许可

MIT — 详见 [LICENSE](LICENSE)
