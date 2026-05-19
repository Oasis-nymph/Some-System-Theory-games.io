# Scaled Dot-Product Attention — 缩放点积注意力热力图

Interactive heatmap visualization of the core mechanism from "Attention Is All You Need" (Vaswani et al., NeurIPS 2017). Step through the computation Q·K^T → Scale by √d_k → Softmax → Attention Weights, across 4 parallel attention heads, with real-time hover details.

来自 Transformer 论文核心机制的交互式热力图可视化。逐步展示 Q·K^T → √d_k 缩放 → Softmax → 注意力权重的完整计算流程，支持 4 个注意力头并排对比，悬停查看每个单元格的精确数值。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/attention-heatmap/)

## The Paper / 论文出处

Vaswani et al., **"Attention Is All You Need"**, NeurIPS 2017, Section 3.2.1–3.2.2.

The core formula:

```
Attention(Q, K, V) = softmax( Q·K^T / √d_k ) · V
```

## How to use / 使用方法

1. **Online / 在线**: open the GitHub Pages link above / 点开上方链接
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## What you see / 可视化内容

| # | Stage | 步骤 | Description |
|---|-------|------|-------------|
| 1 | S = Q·K^T | 原始相似度 | Raw dot-product scores between all token pairs |
| 2 | S / √d_k | 缩放后 | Scaled by 1/√d_k to prevent gradient vanishing |
| 3 | A = softmax(S/√d_k) | 注意力权重 | Row-wise softmax — each row sums to 1 |

| Feature | 功能 |
|---------|------|
| 4 attention heads side-by-side comparison | 4 头并排对比 |
| Hover any cell to see exact value + token pair | 悬停查看精确数值和词对 |
| Pre-built example sentences | 内置示例句子 |
| Custom sentence input | 自定义句子输入 |
| Color scale legend | 色阶图例 |
| Chinese / English toggle | 中英文切换 |

## Keyboard shortcuts / 键盘快捷键

| Key | Action |
|-----|--------|
| `1` `2` `3` | Switch stage / 切换计算步骤 |
| `←` `→` | Switch attention head / 切换注意力头 |
| `R` | Recompute / 重新计算 |

## Technical notes / 技术说明

- **Embedding dimension** d_model = 32
- **Attention heads** h = 4, each d_k = d_v = 8
- Head 0 uses identity projection (semantic head) — QK^T directly reflects embedding similarities
- Heads 1–3 use random Gaussian projections — showing how different subspaces capture different patterns
- Word embeddings are pre-structured into semantic groups (animals, actions, objects, prepositions...) so that attention patterns are visually meaningful
- All projection matrices and embeddings are deterministic (seeded RNG) — the same input always produces the same heatmap
- **Head 0 使用恒等投影** — QK^T 直接反映词嵌入的语义相似度（同类词相互关注）
- **Heads 1–3 使用随机高斯投影** — 展示不同子空间如何捕捉不同注意力模式
- 词汇嵌入按语义组预结构化（动物、动作、物体、介词...），使注意力模式具有视觉可解释性

## Deploy to GitHub Pages / 部署

1. Push this folder to a GitHub repo / 推送文件夹到 GitHub 仓库
2. Settings → Pages → Source: `main` branch, root → Save
3. Visit / 访问 `https://<username>.github.io/<repo>/attention-heatmap/`

---

Created by **BW** | Vaswani et al. "Attention Is All You Need" &copy; 2017 NeurIPS
