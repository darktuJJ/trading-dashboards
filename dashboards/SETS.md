# SETS MACHINE

> 截图均链接自原仓库，未复制到本仓库（SETS 的许可证在 GitHub 上识别为 NOASSERTION）。
> Screenshots are linked from the original repository, not copied (GitHub reports SETS's license as NOASSERTION).

## 基本信息

| 项目 | 内容 |
| --- | --- |
| 仓库 | [darktuJJ/SETS](https://github.com/darktuJJ/SETS)（fork） |
| 上游 | [Shelpid/SETS](https://github.com/Shelpid/SETS) |
| 技术栈 | 纯 HTML / CSS / 原生 JavaScript（ES 模块），`<canvas>` 绘制；无框架、无构建、无 npm 依赖 |
| 运行方式 | `python -m http.server 8000 --directory dist`，浏览器打开 http://localhost:8000 |
| 数据 | 内置 2,399 根 BTCUSDT 1 小时 K 线（Binance 公开接口） |
| 性质 | 演示 / 研究玩具，**不是交易系统**：只做历史数据模拟盘，不连交易所、不下单 |

## 截图

![SETS MACHINE 主界面](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/hero.png)

![基因池动画](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/genepool.gif)

![进化循环与适应度](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/evolution.gif)

更多：[选择漏斗与 Kelly 仓位](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/selection.png) · [模拟网格交易](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/trading.png) · [手机布局](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/mobile.png) · [整页截图](https://raw.githubusercontent.com/darktuJJ/SETS/main/docs/images/dashboard.png)

## 可参考之处

- **遗传算法进化的实时动画**：每 4.8 秒一代，基因池中个体诞生、谱系连线脉冲、淘汰，直观展示 GA 搜索过程。
- **权益曲线与成交标记**：模拟网格面板在 K 线上标出挂单价位、买入、止盈和止损，并附执行日志。
- **适应度历史曲线**：每代最佳 / 平均适应度随时间变化。
- **基因组可视化**：用分段条形显示 8 个基因的取值，领先者变化时高亮发生变异的基因。
- **交互**：运行 / 暂停、单步、1×–8× 速度；点击节点查看其基因组和样本内 / 样本外结果；键盘快捷键；URL 参数（`?seed=`、`?speed=`、`?warm=`、`?paused`）。
- **响应式**：手机上面板自动堆叠，没有横向滚动。
- **零依赖实现**：全部绘图都在一个文件里，便于拆出来学习。

## 关键文件

| 文件 | 作用 |
| --- | --- |
| [`dist/ui/draw.js`](https://github.com/darktuJJ/SETS/blob/main/dist/ui/draw.js) | Canvas 绘图：logo、圆环、适应度曲线、基因池、Kelly 图、K 线图 |
| [`dist/app.js`](https://github.com/darktuJJ/SETS/blob/main/dist/app.js) | 控制器：代际时间线、模拟盘、界面状态 |
| [`dist/style.css`](https://github.com/darktuJJ/SETS/blob/main/dist/style.css) | 蓝白配色的响应式界面 |
| [`dist/engine/evolution.js`](https://github.com/darktuJJ/SETS/blob/main/dist/engine/evolution.js) | 遗传算法：基因组、交叉、变异、物种配额、样本外关卡 |
| [`dist/engine/bot.js`](https://github.com/darktuJJ/SETS/blob/main/dist/engine/bot.js) | 网格 DCA 机器人：信号、网格成交、止盈止损、手续费、指标 |

## 注意事项

- 只有一个标的（BTC）、一次 70/30 划分，样本外只有 30 天；README 自己承认同期买入持有收益更高。
- 上游只有一个“Add files via upload”提交，没有开发历史；作者账号较新。
- 2026-10-12 实测：`node --test` 8 项全部通过，README 中的结果可以复现；代码中没有发现网络请求、密钥或钱包相关逻辑。
