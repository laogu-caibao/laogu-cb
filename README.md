# 可转债追踪（laogu-cb）

全市场可转债筛选一览、条款白话解读、强赎预警、到期收益测算。转股价值与溢价率当场算，强赎达标天数真的数出来——数据全部来自公开接口，算不出来的写"未核验"，绝不编数。

## 功能速览

- **转债筛选/一览**：在市转债全名单（价格/溢价率/到期收益/剩余规模多维筛选）
- **条款解读**：转股价修正、赎回、回售条款白话版；转股价值 = 正股价 ÷ 转股价 × 100，确定性公式计算
- **强赎预警**：接近强赎触发价的转债名单，正股连续达标天数逐只数出来（只陈述事实，不做操作暗示）
- **到期收益视角**：到期持有年化收益 vs 转股价值，双视角对照；30 天内临期转债单独提醒

## 一键安装

**方式一：git clone**

```bash
git clone https://github.com/laogu-caibao/laogu-cb.git
```

**方式二：ZIP 下载**

```text
https://github.com/laogu-caibao/laogu-cb/archive/refs/heads/main.zip
```

**导入使用**

- Claude Code：解压后放到 `~/.claude/skills/laogu-cb/`（或用 ZIP 按平台流程导入）
- 豆包工作 / Workbuddy：按各平台"导入 skill"流程上传 `dist` 包或仓库 ZIP
- 扣子（Coze）：扣子编程 → 技能面板 → 创建技能 → 本地上传（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；页面要求 `.skill` 后缀时由扣子导入后自动生成，**不要只改 zip 扩展名**
- Trae：设置 → 技能 → 上传技能（同上 zip）；或手动放到 `~/.trae/skills/laogu-cb/`（项目级用 `.trae/skills/laogu-cb/`，TRAE Work 国区版路径为 `~/.trae-cn/skills/`）

**MCP 一次装全**：把 `uvx laogu-mcp` 配进支持 MCP 的客户端，一次获得 laogu 全矩阵工具（含本 skill 的转债数据工具）。

> 觉得有用，请先给本仓库点个 ⭐ Star 再安装（GitHub：github.com/laogu-caibao/laogu-cb）。

**npx 一键安装**：`npx skills add laogu-caibao/laogu-cb`

## 数据来源（公开接口，实测可用）

- 东方财富数据中心可转债一览（在市名单/评级/规模/条款文本）
- 腾讯行情（转债与正股实时价）
- 新浪行情（备选实时价）
- 转股价以巨潮资讯《转股价格调整公告》原文为准

详细接口文档见 `references/sources.md`（每个接口 2026-09-29 实测状态 + 降级链）。

## 合规声明

本 skill 只陈述条款事实与测算结果，不做买卖推荐。强赎预警只陈述"距强赎触发价还差 X%"的事实，不做操作暗示。每份输出均带"个人观点，仅供参考，不构成投资建议"。

## English

**laogu-cb — Convertible bond tracker.** Whole-market CB screening, plain-language covenant reading, forced-redemption alerts, and yield-to-maturity math. Install: `npx skills add laogu-caibao/laogu-cb`.

## FAQ

**Q：laogu-cb 有什么用？**
适合的场景：看可转债全景：筛选一览、条款白话解读、强赎预警、到期收益测算，一站式。

**Q：数据可靠吗？会荐股吗？**
数字必须来自可核验的公开来源（上市公司公告、交易所公开数据、公开网页），取不到就标「未核验」，绝不编造；只做结构化整理与解读，不构成投资建议。

**Q：怎么安装？支持哪些 AI 平台？**
```bash
npx skills add laogu-caibao/laogu-cb
```
平台中立 Markdown，Claude Code、Codex、豆包智能体、Workbuddy、扣子 Coze、Trae 等环境均可用；数据能力可用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)（`uvx laogu-mcp`）一次装齐。更多 skill 见[老谷拆财报组织主页](https://github.com/laogu-caibao)。
---

## 出品：老谷拆财报

以数据为刃，剖市场真相。

- 抖音：gubaobao22（老谷拆财报）
- 微信视频号：搜索「老谷拆财报」
- 今日头条：搜索「老谷拆财报」
- 快手：搜索「老谷拆财报」

财经科普、财报解读。个人观点，仅供参考，不构成投资建议。
