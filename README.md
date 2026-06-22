# 估值技能看板

一个中文优先的本地看板，用来快速使用股票估值相关 Codex skills：

- DCF 估值
- SEC 财报分析
- 投资备忘录

打开 `index.html` 即可使用。

## 使用方式

1. 选择一个技能卡片。
2. 点击复制提示词。
3. 把股票代码、财报链接或估值假设替换进去。
4. 发给 Codex 执行分析。

## 自动联网粗估值

页面顶部提供一个实验性的自动估值模块：

1. 输入美股 ticker，例如 `NBIS`。
2. 点击「自动抓取并估值」。
3. 页面会尝试读取公开数据，并用可编辑假设跑三情景 DCF。

当前数据源：

- SEC `company_tickers.json` 和 `companyfacts`：用于匹配 CIK、读取收入和股数。
- Yahoo Finance chart 公开接口：用于读取延迟价格。

限制：

- 这是 GitHub Pages 静态前端，没有后端和 API key。
- 公开接口可能受 CORS、SEC/Yahoo 限流、ticker 覆盖范围或延迟报价影响。
- 自动结果只是教育用途的粗估值，不是投资建议。
- 抓不到数据时，可以手动填写收入、股数、价格、WACC、利润率等假设继续计算。

## 文件

- `index.html`: 看板页面
- `concept.png`: 视觉概念图
