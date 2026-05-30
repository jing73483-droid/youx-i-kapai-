# CLAUDE.md — 小丑牌 (Balatro)

单文件扑克+小丑牌 Roguelike 游戏。

## 项目定位

Balatro 风格核心循环游戏，教学项目第 1 轮产出。纯前端、零依赖、单 HTML 文件。

## 目录约定

```
index.html     # 完整游戏（HTML + CSS + JS 内嵌，~1100 行）
.gitignore     # 忽略规则
README.md      # 项目说明
```

## 技术栈

- 原生 HTML/CSS/JavaScript（无框架）
- Google Fonts：Press Start 2P / VT323 / Inter
- 无构建工具、无后端、无 API 依赖

## 核心架构

- 全局状态对象 `G`：deck / hand / jokers / money / state 等
- 状态机：`playing` → `shop` → `playing` → `won` / `lost`
- 渲染函数：`renderAll()` / `renderSidebar()` / `renderHand()` 等
- 动画函数：`dealNewCards()` / `discardCards()` / `animateCardsFromDeck()`

## 常用命令

```bash
# 本地预览
open index.html

# 如需本地服务器
python3 -m http.server 8000
```
