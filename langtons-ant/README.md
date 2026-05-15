# Langton's Ant 兰顿蚂蚁

Langton's Ant — a two-dimensional Turing machine and cellular automaton devised by Chris Langton in 1986. An "ant" moves on a grid of black and white cells following two simple rules, producing emergent behavior that transitions from chaotic patterns to an ordered "highway" after ~10,000 steps. Turing completeness was proved in 2000.

兰顿蚂蚁 — 克里斯托夫·兰顿 1986 年提出的细胞自动机模型。蚂蚁在黑白格子上依据两条简单规则移动：黑格右转、白格左转，翻转格子颜色后前进一步。约一万步后从混沌对称模式进入以 104 步为周期的"高速公路"无限延伸。2000 年证实其图灵完备。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/langtons-ant/)

## How to use / 使用方法

1. **Online / 在线**: open the GitHub Pages link above / 点开上方链接即可
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## Rules / 规则

| # | English | 中文 |
|---|---------|------|
| 1 | On a black cell: turn right 90°, flip to white | 处于黑格：右转 90°，变为白格 |
| 2 | On a white cell: turn left 90°, flip to black | 处于白格：左转 90°，变为黑格 |
| 3 | Move forward one step | 向前移动一步 |
| 4 | After ~10,000 steps, forms a 104-step periodic highway | 约一万步后进入 104 步周期的高速公路 |

## Features / 功能

- Canvas-based rendering / Canvas 渲染
- Directional triangle ant indicator / 三角形方向指示
- Click and drag to paint black/white cells / 鼠标拖动绘制黑白格子
- Right-click or double-click to move the ant / 右键或双击移动蚂蚁
- Adjustable simulation speed / 可调速度
- Chinese / English language toggle / 中英文切换
- Keyboard shortcuts (Space / S / R / C) / 键盘快捷键
- Highway detection badge after 10,000 steps / 10000 步后高速公路标记
- Responsive layout for desktop & mobile / 响应式布局
- Toroidal grid (wraps around edges) / 环面网格（边界环绕）

## Keyboard Shortcuts / 快捷键

| Key | Action / 操作 |
|-----|---------------|
| Space | Play / Pause 开始/暂停 |
| S | Step forward 前进一步 |
| R | Random grid 随机布局 |
| C | Clear grid 清空 |

## Deploy to GitHub Pages / 部署

1. Push this folder to a GitHub repo / 推送文件夹到 GitHub 仓库
2. Settings → Pages → Source: `main` branch, root → Save / 设置 Pages 分支保存
3. Visit / 访问 `https://<username>.github.io/<repo>/langtons-ant/`

## Background / 背景

- **1986** — Chris Langton proposes the ant as a simple cellular automaton
- **2000** — Gajardo et al. prove Langton's Ant is Turing-complete
- The ant's trajectory is an open question: for any initial configuration of black/white cells, does the ant always eventually build a highway? (unproven)

---

Created by **BW** | Langton's Ant &copy; 1986 Chris Langton
