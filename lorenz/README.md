# Lorenz Attractor — 洛伦兹吸引子三维可视化

Edward Lorenz's 1963 system of three coupled ODEs is the iconic example of **deterministic chaos**: simple equations, no randomness, yet the trajectory never repeats and is exquisitely sensitive to initial conditions — the **butterfly effect**.

爱德华·洛伦兹 1963 年提出的三变量耦合常微分方程是**确定混沌**的经典范例：方程简单、无随机项，但轨迹永不重复，且对初始条件极度敏感——即**蝴蝶效应**。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/lorenz/)

## How to use / 使用方法

1. **Online / 在线**: open the GitHub Pages link above / 点开上方链接即可
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## The Lorenz System / 洛伦兹系统

| | General Form / 一般形式 | With Default Values / 带入默认值 |
|---|---------|------|
| 1 | d*x*/dt = σ(*y* − *x*) | d*x*/dt = **10.0**(*y* − *x*) |
| 2 | d*y*/dt = *x*(ρ − *z*) − *y* | d*y*/dt = *x*(**28.0** − *z*) − *y* |
| 3 | d*z*/dt = *xy* − β*z* | d*z*/dt = *xy* − **2.67***z* |

| Parameter / 参数 | Symbol | Default | Meaning / 含义 |
|---|:---:|:---:|---|
| Sigma / 西格玛 | σ | 10 | Prandtl number — viscous vs. thermal diffusion / 普朗特数，粘性与热扩散比 |
| Rho / 密度比 | ρ | 28 | Rayleigh number — temperature gradient driving force / 瑞利数，温差驱动力 |
| Beta / 阻尼比 | β | 8/3 | Geometric factor — z-direction damping / 几何因子，z 向衰减速度 |

> **ρ > 24.74** → chaos emerges / 混沌出现 ｜ Initial divergence demo: Δx₀ = 0.001 / 初始偏差演示：Δx₀ = 0.001

## Features / 功能

- 3D WebGL rendering with **bloom post-processing** — trajectories glow like neon tubes in deep space / 三维 WebGL + **泛光后处理**，轨迹如霓虹管悬浮深空
- **RK4** (4th-order Runge-Kutta) numerical integration / **RK4** 四阶龙格-库塔数值积分
- Two trajectories from slightly different initial conditions demonstrate the butterfly effect / 两条轨迹初始仅差 0.001，直观演示蝴蝶效应
- 3 adjustable parameters (σ, ρ, β) with real-time trajectory reset / 3 个可调参数，实时重置轨迹
- Orbit controls: drag to rotate, scroll to zoom, right-drag to pan / 轨道控制：拖拽旋转、滚轮缩放、右键平移
- Auto-rotate when idle / 静止时自动旋转
- Starfield background + reference grid + coordinate axes / 星场背景 + 参考网格 + 坐标轴
- Glowing head particles at trajectory tips / 轨迹头部脉冲光点
- Bilingual UI: Chinese (default) / English toggle / 中英文双语界面（中文默认）
- Built-in detailed documentation panel (history, parameters, chaos, interaction) / 内嵌详细介绍文档（历史、参数、混沌、交互）
- Keyboard shortcuts (Space = pause, R = reset, C = clear) / 键盘快捷键
- Responsive layout for desktop & mobile / 响应式布局，桌面/移动端适配
- **Single HTML file** — zero dependencies, zero build / **单 HTML 文件**，零依赖，零构建

## Deploy to GitHub Pages / 部署

1. Push this folder to a GitHub repo / 推送文件夹到 GitHub 仓库
2. Settings → Pages → Source: `main` branch, root → Save / 设置 Pages 选 main 分支根目录保存
3. Visit / 访问 `https://<username>.github.io/<repo>/lorenz/`

---

Created by **BW** | Lorenz — Edward Lorenz 1963
