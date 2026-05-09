# 五子棋游戏 (Gomoku)

一款基于 HTML/CSS/JavaScript 开发的网页版五子棋游戏，无需安装任何环境，开箱即用！


![游戏版本](https://img.shields.io/badge/version-1.0.0-blue)
![HTML5](https://img.shields.io/badge/HTML5-Compatible-green)
![License](https://img.shields.io/badge/license-MIT-yellow)
## 简介

五子棋是一种两人对弈的纯策略型棋类游戏，双方分别使用黑白两色棋子，下在棋盘纵横交叉的交叉点上，先形成五子连线者获胜。

本游戏完全使用前端技术开发，只需一个浏览器即可畅玩。

## 功能特点

### 核心功能

- 鼠标操作：点击棋盘交叉点即可落子，操作简单直观
- 计时系统：可自定义每步思考时间（10-600秒），超时自动判负
- 记分功能：自动记录双方胜场数，数据本地持久化保存
- 对局记录：实时显示每步落子坐标和思考时间
- 悔棋功能：支持撤销操作，每次可回退两步
- 认输功能：可提前结束对局
- 游戏设置：自定义玩家名称和时间限制
- 数据导出：支持导出为 TXT 和 JSON 格式
- 本地存储：设置和分数自动保存到浏览器本地

### 界面特色

- 精美 UI 设计：现代化渐变背景，圆角卡片布局
- 实时状态反馈：棋盘高亮显示最后落子位置
- 动态计时器：根据剩余时间变换颜色（绿->黄->红）
- 流畅动画：棋子落下的阴影效果，按钮悬停动画
- 获胜提示：弹出对话框询问是否开始下一局

## 游戏规则

### 基本规则

1. 棋盘：15 x 15 的网格棋盘
2. 棋子：黑白两色棋子，黑棋先行
3. 落子：双方交替落子，每次只能落一子
4. 位置：棋子必须落在棋盘的空交叉点上

### 胜负判定

- 五子连珠：先形成五子连线（横、竖、斜）的一方获胜
- 超时判负：超过规定思考时间未落子，该方判负
- 认输：主动认输，对方获胜
- 平局：棋盘填满且无人五子连珠，判定平局

### 五子连珠示意

```
横线连珠：
● ● ● ● ●

竖线连珠：
●
●
●
●
●

正斜连珠：
●
  ●
    ●
      ●
        ●

反斜连珠：
        ●
      ●
    ●
  ●
●
```

## 快速开始

### 方法一：直接打开

1. 下载 gomoku-mimo.html 文件
2. 双击文件，使用浏览器打开
3. 开始游戏！

### 方法二：拖拽打开

1. 将 gomoku-mimo.html 文件拖拽到浏览器窗口
2. 游戏自动加载

### 方法三：右键打开

1. 右键点击 gomoku-mimo.html 文件
2. 选择"打开方式" -> 选择任意浏览器

推荐使用 Chrome、Firefox、Edge 等现代浏览器获得最佳体验。

## 操作说明

### 基本操作

- 落子：鼠标左键点击棋盘交叉点
- 新游戏：点击"新游戏"按钮
- 悔棋：点击"悔棋"按钮（每次回退两步）
- 认输：点击"认输"按钮
- 设置：点击"设置"按钮修改游戏参数

### 导出记录

1. 点击"导出TXT"或"导出JSON"按钮
2. 浏览器会自动下载对局记录文件
3. 文件保存在浏览器默认下载目录

## 界面说明

### 主界面布局

```
+--------------------------------------------------------------+
|                       五子棋游戏                              |
+------------------------------+-------------------------------+
|                              |  玩家信息                     |
|      A B C D E F G ...      |  +-------------------------+ |
|   1  . . . . . . . . .      |  | 黑棋                0   | |
|   2  . . . . . . . . .      |  | 白棋                0   | |
|   3  . . . . . . . . .      |  +-------------------------+ |
|   4  . . . ● . . . . .      |                               |
|   5  . . . . ○ . . . .      |  计时器                       |
|         棋盘区域             |  +-------------------------+ |
|                              |  |        00:45            | |
|                              |  |    每步限时: 60秒        | |
|                              |  +-------------------------+ |
|                              |                               |
|                              |  游戏操作                     |
|                              |  +--------+--------+         |
|                              |  | 新游戏  | 悔棋   |         |
|                              |  +--------+--------+         |
|                              |  | 认输    | 设置   |         |
|                              |  +--------+--------+         |
|                              |                               |
|                              |  对局记录                     |
|                              |  +-------------------------+ |
|                              |  | #1 黑棋   H8   3.2s    | |
|                              |  | #2 白棋   I9   5.1s    | |
|                              |  +-------------------------+ |
|                              |  [导出TXT] [导出JSON]        |
+------------------------------+-------------------------------+
```

### 计时器颜色说明

- 绿色（>30秒）：时间充足
- 黄色（10-30秒）：时间紧张
- 红色闪烁（<10秒）：时间紧迫

## 游戏设置

### 可设置项目

- 黑棋玩家名称：任意文字，默认"黑棋"
- 白棋玩家名称：任意文字，默认"白棋"
- 每步思考时间：10-600秒，默认60秒

### 预设时间选项

- 30秒（快棋模式）
- 60秒（标准模式）
- 120秒（慢棋模式）
- 180秒（长考模式）

## 导出格式

### TXT 格式示例

```
==================================================
                   五子棋对局记录
==================================================
黑棋: 玩家A
白棋: 玩家B
每步限时: 60秒
--------------------------------------------------

落子记录:
--------------------------------------------------
#     棋手          坐标    思考时间
--------------------------------------------------
1     玩家A(黑棋)   H8      3.2秒
2     玩家B(白棋)   I9      5.1秒
--------------------------------------------------
总手数: 2
==================================================
```

### JSON 格式示例

```json
{
  "gameInfo": {
    "blackName": "玩家A",
    "whiteName": "玩家B",
    "timeLimit": 60
  },
  "moves": [
    {
      "moveNumber": 1,
      "player": "Black",
      "playerName": "玩家A",
      "coordinate": "H8",
      "thinkingTime": 3.2
    }
  ],
  "result": {
    "totalMoves": 1
  }
}
```

## 数据存储

游戏使用浏览器 localStorage 存储以下数据：

- 玩家名称设置
- 双方胜场数
- 时间限制设置

注意：清除浏览器缓存会丢失存储的数据，建议定期使用导出功能备份对局记录。

## 浏览器兼容性

- Chrome 60+：完全支持
- Firefox 55+：完全支持
- Edge 79+：完全支持
- Safari 11+：完全支持
- IE 11：部分支持（不推荐）

## 游戏技巧

### 新手建议

1. 抢占中心：开局尽量占据棋盘中心位置
2. 攻守兼备：既要组织进攻，也要注意防守
3. 观察全局：不要只盯着一处，注意整体布局
4. 利用双三：同时形成两个活三是强力进攻手段

## 常见问题

### Q: 游戏数据会丢失吗？

A: 游戏设置和分数保存在浏览器本地存储中，清除浏览器数据会导致丢失。建议定期使用导出功能备份对局记录。

### Q: 可以多人游戏吗？

A: 本游戏是本地双人对战模式，两位玩家在同一设备上轮流操作。

### Q: 支持移动端吗？

A: 支持，但由于棋盘较大，建议在平板或电脑上使用获得更好体验。

### Q: 如何修改时间限制？

A: 点击"设置"按钮，在弹出的对话框中修改"每步思考时间"。

## 许可证

本项目采用 MIT 许可证。

MIT License

Copyright (c) 2024 Gomoku Game

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

**祝您游戏愉快！**
