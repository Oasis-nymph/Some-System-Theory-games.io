# SFI Double Auction Tournament / SFI 双向拍卖模拟

Rust-Miller-Palmer (1992-1994) synchronized double auction market simulation. Runs entirely in the browser — no server, no install, no dependencies.

Rust-Miller-Palmer (1992-1994) 同步双向拍卖市场模拟。纯浏览器运行，无服务器、无安装、无依赖。

[**Live Demo / 在线演示**](https://oasis-nymph.github.io/Some-System-Theory-games.io/double_auction/)

## How to use / 使用方法

1. **Online / 在线**: just open the GitHub Pages link above / 点开上方链接即可
2. **Local / 本地**: download `index.html` and double-click it / 下载 index.html 双击打开

## Background / 背景

The Santa Fe Institute Double Auction Tournament involved 30 computer trading programs competing in a synchronized double auction. Key findings:

圣塔菲研究所 (SFI) 双向拍卖锦标赛汇集了 30 个计算机交易程序，在同步双向拍卖中竞争。核心发现：

- **Near-100% allocative efficiency** emerges from the auction mechanism itself / **接近 100% 的配置效率**源于拍卖机制本身
- **Simple strategies (Kaplan sniper) consistently outperform complex ones** (Bayesian learners, profit-maximizers) / **简单策略（Kaplan 狙击手）持续优于复杂策略**（贝叶斯学习器、利润最大化器）
- The double auction institution — not trader intelligence — drives market efficiency / 双向拍卖制度本身 — 而非交易者智能 — 驱动市场效率

Reference / 参考文献: Rust, J., Miller, J.H., & Palmer, R. (1994), *Journal of Economic Dynamics and Control*, 18(1), 61-96.

## Strategies / 策略

| Strategy / 策略 | Complexity / 复杂度 | Description / 描述 |
|----------|------------|-------------|
| Fundamental / 基本面 | Medium / 中 | Estimates P* from history, bids with margin / 从历史估算均衡价格，加边际出价 |
| Bayesian / 贝叶斯 | Medium / 中 | Normal belief over P*, Kalman-style updating / 正态分布信念，类卡尔曼更新 |
| ProfitMax / 利润最大化 | High / 高 | Numerical expected-profit maximization / 数值期望利润最大化 |
| Kaplan Sniper / Kaplan狙击 | Low / 低 | Waits until spread < 15%, then steals the deal / 等待价差 < 15%，然后抢单 |
| ZI-C / 零智能 | Minimal / 极低 | Random bids/asks within budget constraint / 预算约束内随机出价 |

## Deploy to GitHub Pages / 部署

1. Push this repo to GitHub / 推送仓库到 GitHub
2. Settings → Pages → Source: `main` branch, root folder → Save / 设置 Pages 选 main 分支根目录保存
3. Visit / 访问 `https://<username>.github.io/<repo>/double_auction/`
