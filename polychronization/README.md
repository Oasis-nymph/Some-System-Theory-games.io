# Polychronization — 多时同步组

**Izhikevich (2006) Polychronization Model** — a large-scale spiking neural network where STDP + conduction delays give rise to "polychronous groups": time-coded memory traces that reveal how information may be encoded in time, not space.

**Izhikevich (2006) 多时同步组模型** — 大规模脉冲神经网络中，STDP 时序依赖可塑性 + 传导延迟涌现出"多时同步组"：同一群神经元因不同延迟参与多个不同的时间序列模式，揭示记忆痕迹可能编码在时间而非空间中。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/polychronization/)

## How to use / 使用方法

1. **Online / 在线**: open the GitHub Pages link above / 点开上方链接即可
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## Background / 背景

In 2006, Eugene Izhikevich published a landmark paper showing that conduction delays in the brain are not just an inconvenience — they are a computational resource. Because different axons have different delays (1-20ms), the same group of neurons can fire in multiple distinct temporal sequences (polychronous groups), each encoding a different memory. This means the brain's memory capacity far exceeds the number of synapses — **time itself becomes an information carrier**.

2006 年，Eugene Izhikevich 发表里程碑论文，证明传导延迟不是大脑计算的不便——而是一种计算资源。由于不同轴突有不同延迟（1-20ms），同一群神经元可以按不同的时间序列模式发放（多时同步组），每种模式编码不同的记忆。这意味着大脑的记忆容量远超突触数量——**时间本身成为信息载体**。

Reference / 参考文献: Izhikevich, E.M. (2006), *Neural Computation* 18(2):245-282 · Cited >3000

## The Model / 模型

### Izhikevich Neuron / Izhikevich 神经元

```
v' = 0.04v² + 5v + 140 - u + I_syn + I_ext
u' = a(bv - u)
若 v ≥ 30mV → v=c, u+=d（发放 / spike!）
```

- 80% Excitatory (RS type) / 兴奋性（常规发放型）
- 20% Inhibitory (FS type) / 抑制性（快速发放型）

### STDP Learning / STDP 学习规则

- **LTP (pre→post)**: Δw = A⁺·exp(-Δt/τ⁺) — 因果增强
- **LTD (post→pre)**: Δw = -A⁻·exp(Δt/τ⁻) — 反因果减弱
- Excitatory synapses only / 仅兴奋性突触

### Conduction Delays / 传导延迟

Each synapse has a random delay (1-20ms), implemented via ring buffer. This is the key ingredient that makes polychronization possible.

每个突触有随机延迟（1-20ms），通过环形缓冲实现。这是多时同步组得以涌现的关键。

## Preset Templates / 预设模板

| # | Template / 模板 | Phenomenon / 现象 | Key Paper / 关键文献 |
|---|----------------|-------------------|---------------------|
| 1 | Balanced Network / 平衡网络 | Irregular asynchronous firing, CV≈1 | van Vreeswijk & Sompolinsky (1996) |
| 2 | Synchronous Bursting / 同步爆发 | Periodic global synchrony (γ-band) | Fries (2005) |
| 3 | **Polychronous Groups** / **多时同步组** | Same neurons, different temporal patterns | **Izhikevich (2006)** |
| 4 | Neuronal Avalanches / 神经元雪崩 | Power-law avalanche size distribution | Beggs & Plenz (2003) |
| 5 | Quiet State / 静默状态 | Sparse coding, ultra-low firing rates | Olshausen & Field (1996) |
| 6 | Seizure-like / 癫痫样活动 | Hyper-synchronization, E/I imbalance | Traub & Wong (1982) |
| 7 | Custom / 自定义 | Free parameter exploration / 自由探索 | — |

## Features / 功能

- **4-panel visualization**: Spike raster, firing rate, weight matrix, polychronous groups / 四面板可视化：脉冲栅格图、发放率曲线、权重矩阵热力图、多时同步组列表
- **Classic results explanation**: Each template comes with bilingual scientific context and references / 每个模板附带中英双语经典结果解释和参考文献
- **7 preset templates** + full custom mode with 6 adjustable parameters / 7 个预设模板 + 6 个可调参数的自定义模式
- **Real-time STDP**: Watch synaptic weights evolve as the network learns / 实时 STDP：观察突触权重随学习演化
- **Polychronous group detection**: Stimulate and detect time-locked neuronal assemblies / 多时同步组检测：刺激并检测时间锁定的神经元群组
- **Chinese / English language toggle** / 中英文切换
- **Keyboard shortcuts** (Space / S / R / 1-6 / 0 / →) / 键盘快捷键
- **Dark theme**, responsive layout for desktop & mobile / 暗色主题，桌面端和移动端响应式
- **Zero dependencies** — single HTML file / 零依赖 — 单 HTML 文件

## Keyboard Shortcuts / 键盘快捷键

| Key / 键 | Function / 功能 |
|-----------|----------------|
| Space | Play / Pause / 播放/暂停 |
| S | Stimulate / 施加刺激 |
| R | Reset / 重置 |
| 1-6 | Switch to preset template / 切换到预设模板 |
| 0 | Custom mode / 自定义模式 |
| → | Step forward / 单步仿真 |

## Deploy to GitHub Pages / 部署

1. Push this folder to a GitHub repo / 推送文件夹到 GitHub 仓库
2. Settings → Pages → Source: `main` branch, root folder → Save / 设置 Pages 选 main 分支根目录保存
3. Visit / 访问 `https://<username>.github.io/<repo>/polychronization/`

---

Created by **BW** | Izhikevich Polychronization Model &copy; 2006

## References / 参考文献

- Izhikevich, E.M. (2006). Polychronization: Computation with Spikes. *Neural Computation*, 18(2), 245-282.
- Izhikevich, E.M. (2004). Which Model to Use for Cortical Spiking Neurons? *IEEE Transactions on Neural Networks*, 15(5), 1063-1070.
- van Vreeswijk, C. & Sompolinsky, H. (1996). Chaos in Neuronal Networks with Balanced Excitatory and Inhibitory Activity. *Science*, 274(5293), 1724-1726.
- Beggs, J.M. & Plenz, D. (2003). Neuronal Avalanches in Neocortical Circuits. *Journal of Neuroscience*, 23(35), 11167-11177.
- Fries, P. (2005). A Mechanism for Cognitive Dynamics: Neuronal Communication Through Neuronal Coherence. *Trends in Cognitive Sciences*, 9(10), 474-480.
- Olshausen, B.A. & Field, D.J. (1996). Emergence of Simple-Cell Receptive Field Properties by Learning a Sparse Code for Natural Images. *Nature*, 381, 607-609.
