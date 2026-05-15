# Boids Flocking Simulation — 鸟群涌现模拟

Craig Reynolds' 1986 boids algorithm demonstrates **emergence**: three simple local rules produce realistic, complex flocking behavior. No leader, no global plan — just local interactions.

Craig Reynolds 1986 年的 Boids 算法展示了**涌现**现象：三条简单的局部规则产生逼真的复杂群集行为。没有领导者，没有全局计划——只有局部交互。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/boids/)

## How to use / 使用方法

1. **Online / 在线**: open the GitHub Pages link above / 点开上方链接即可
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## The Three Rules / 三条规则

| # | English | 中文 |
|---|---------|------|
| 1 | **Separation**: steer away from nearby flockmates to avoid crowding | **分离**：近邻太近 → 转向远离，避免碰撞 |
| 2 | **Alignment**: steer toward the average heading of neighbors | **对齐**：匹配近邻平均航向 → 朝同一方向飞 |
| 3 | **Cohesion**: steer toward the average position of neighbors | **凝聚**：朝近邻平均位置靠拢 → 聚集成群 |

## Features / 功能

- Canvas-based rendering with spatial hashing for O(n) performance / Canvas 渲染 + 空间哈希 O(n) 加速
- 6 adjustable parameters (separation, alignment, cohesion, perception radius, max speed, steering force) / 6 个可调参数
- Predator mode — boids flee from a chasing predator / 捕食者模式
- Trail mode — visualize boid trajectories / 尾迹模式
- Perception radius visualization / 感知半径可视化
- Mouse interaction: left-click attract, right-click repel / 鼠标交互：左键吸引，右键驱散
- Real-time flock counting via Union-Find clustering / Union-Find 实时鸟群计数
- Chinese / English language toggle / 中英文切换
- Keyboard shortcuts (Space/S/R/A/P/T/D) / 键盘快捷键
- Responsive layout for desktop & mobile / 响应式布局

## Deploy to GitHub Pages / 部署

1. Push this folder to a GitHub repo / 推送文件夹到 GitHub 仓库
2. Settings → Pages → Source: `main` branch, root → Save / 设置 Pages 选 main 分支根目录保存
3. Visit / 访问 `https://<username>.github.io/<repo>/boids/`

---

Created by **BW** | Boids — Craig Reynolds 1986
