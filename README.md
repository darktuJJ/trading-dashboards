**简体中文** · [English](README.en.md)

# trading-dashboards

收集我看到的交易 / 策略仪表盘界面，作为设计和实现上的参考。

## 用途

- 记录值得借鉴的交易类仪表盘（回测、实盘监控、策略进化、风险面板等）。
- 关注**界面和可视化**本身：布局、图表、动画、交互方式和实现技术。
- 只做参考收藏，不代表推荐其中的策略，也不对其交易表现负责。

## 收录方式

- 每个条目在 [`dashboards/`](dashboards/) 下有一个独立的 Markdown 文件，例如 [`dashboards/SETS.md`](dashboards/SETS.md)，记录来源、技术栈、亮点、关键文件和注意事项。
- 下面的索引表每个条目一行，链接到对应的详情文件。
- 截图优先**链接到原仓库**的图片，不直接复制进本仓库，以免产生许可证问题。

## 索引

| 名称 | 链接 | 技术栈 | 亮点 / 可参考之处 | 截图 | 备注 |
| --- | --- | --- | --- | --- | --- |
| [SETS MACHINE](dashboards/SETS.md) | [darktuJJ/SETS](https://github.com/darktuJJ/SETS)（上游 [Shelpid/SETS](https://github.com/Shelpid/SETS)） | 纯 HTML / CSS / 原生 JavaScript，`<canvas>` 绘制（[`dist/ui/draw.js`](https://github.com/darktuJJ/SETS/blob/main/dist/ui/draw.js)） | 遗传算法进化过程的实时动画（基因池、谱系、适应度曲线）；权益曲线和买卖点标记；无框架、无构建 | [主界面](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/hero.png) · [基因池 GIF](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/genepool.gif) | 演示项目，不是交易系统：只用历史 BTC 数据做模拟盘 |

## 添加新条目

1. 在 `dashboards/` 下新建 `<名称>.md`，可参考 [`dashboards/SETS.md`](dashboards/SETS.md) 的结构。
2. 在上面的索引表中加一行。
3. 截图用原仓库的链接；只有确认许可证允许时才复制图片。

## 许可证

本仓库自己的内容采用 [MIT 许可证](LICENSE)。各条目引用的项目、截图和代码归其原作者所有，适用其各自的许可证。
