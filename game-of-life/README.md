# Conway's Game of Life 康威生命游戏

Conway's Game of Life — a zero-player cellular automaton devised by mathematician John Conway in 1970. Patterns evolve on a 2D grid following four simple rules, producing surprisingly complex emergent behavior.

康威生命游戏 — 英国数学家约翰·康威 1970 年发明的"零玩家游戏"。只需初始布局和四条简单规则，细胞在二维网格中自动演化，涌现出惊人的复杂结构。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/game-of-life/)

## How to use / 使用方法

1. **Online / 在线**: open the GitHub Pages link above / 点开上方链接即可
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## The Four Rules / 四条规则

| # | English | 中文 |
|---|---------|------|
| 1 | Any live cell with < 2 live neighbors dies (underpopulation) | 活细胞周围活邻居少于 2 个 → 因孤立而死亡 |
| 2 | Any live cell with 2 or 3 live neighbors lives on | 活细胞周围有 2 或 3 个活邻居 → 存活到下一代 |
| 3 | Any live cell with > 3 live neighbors dies (overpopulation) | 活细胞周围活邻居多于 3 个 → 因拥挤而死亡 |
| 4 | Any dead cell with exactly 3 live neighbors becomes alive | 死细胞周围恰好有 3 个活邻居 → 重新复活 |

## Features / 功能

- Canvas-based rendering / Canvas 渲染
- Draw cells with mouse/touch / 鼠标/触摸绘制细胞
- Adjustable simulation speed / 可调速度
- Chinese / English language toggle / 中英文切换
- Keyboard shortcuts (Space / S / R / C) / 键盘快捷键
- Responsive layout for desktop & mobile / 响应式布局

## Deploy to GitHub Pages / 部署

1. Push this folder to a GitHub repo / 推送文件夹到 GitHub 仓库
2. Settings → Pages → Source: `main` branch, root → Save / 设置 Pages 分支保存
3. Visit / 访问 `https://<username>.github.io/<repo>/game-of-life/`

---

Created by **BW** | Conway's Game of Life &copy; 1970
