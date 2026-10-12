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
- 截图放在 [`dashboards/assets/`](dashboards/assets/) 下，按条目分目录，并在详情文件中注明来源和版权。

## 索引

| 名称 | 链接 | 技术栈 | 亮点 / 可参考之处 | 截图 | 备注 |
| --- | --- | --- | --- | --- | --- |
| [SETS MACHINE](dashboards/SETS.md) | [Shelpid/SETS](https://github.com/Shelpid/SETS) | 纯 HTML / CSS / 原生 JavaScript，`<canvas>` 绘制（[`dist/ui/draw.js`](https://github.com/Shelpid/SETS/blob/main/dist/ui/draw.js)） | 遗传算法进化过程的实时动画（基因池、谱系、适应度曲线）；权益曲线和买卖点标记；无框架、无构建 | [主界面](dashboards/assets/SETS/hero.png) · [基因池 GIF](dashboards/assets/SETS/genepool.gif) · [演示视频](dashboards/assets/SETS/sets-machine-promo.mp4) | 演示项目，不是交易系统：只用历史 BTC 数据做模拟盘 |

## 添加新条目

1. 在 `dashboards/` 下新建 `<名称>.md`，可参考 [`dashboards/SETS.md`](dashboards/SETS.md) 的结构。
2. 在上面的索引表中加一行。
3. 截图放进 `dashboards/assets/<名称>/`，并注明来源；原作者要求时立即删除。

## 许可证

本仓库自己的内容采用 [MIT 许可证](LICENSE)。各条目引用的项目、截图、视频和代码归其原作者所有，不在 MIT 许可范围内。
