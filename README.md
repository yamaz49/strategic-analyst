# Strategic Analyst

<p align="center">
  <b>你的随身麦肯锡顾问</b><br>
  Claude Code 战略分析 Skill | 行业分析 · 竞争格局 · 投资决策 · 市场进入
</p>

<p align="center">
  <a href="#快速开始">🚀 快速开始</a> •
  <a href="#核心能力">✨ 核心能力</a> •
  <a href="#使用示例">📊 使用示例</a> •
  <a href="#分析框架">🧩 分析框架</a> •
  <a href="#前置要求">⚙️ 前置要求</a>
</p>

---

## 简介

**Strategic Analyst** 是一个为 [Claude Code](https://claude.ai/code) 设计的战略分析 Skill。

它能够像麦肯锡顾问一样，帮助你系统性地分析一个行业、评估竞争格局、测算市场规模、并为关键商业决策提供数据支撑。

无论你是：
- 🏢 **企业高管** — 评估新市场进入机会
- 💼 **投资人** — 快速建立对陌生行业的认知
- 🎓 **学生/研究者** — 学习战略分析框架的实际应用
- 🚀 **创业者** — 寻找差异化定位和竞争策略

这个 Skill 都能在 **10-20 分钟** 内帮你产出一份结构完整、数据可溯源的专业分析报告。

---

## 核心能力

- 🔍 **需求智能诊断**：自动识别你的身份和决策问题，调整分析深度
- 📚 **6 大经典框架**：波特五力、TAM-SAM-SOM、竞争格局、PESTEL、价值链、关键成功因素
- 🌐 **实时数据增强**：集成 Tavily 深度搜索，自动获取最新行业数据和竞争动态
- 📑 **强制数据溯源**：所有关键数据必须标注来源、时效和可信度星级
- 📄 **双格式报告输出**：同时生成 Markdown 和 HTML 专业报告
- 🚧 **质量门禁系统**：输出前自动检查结构完整性、数据支撑和专业边界

---

## 快速开始

### 安装 Skill

将本仓库克隆到 Claude Code 的 skills 目录：

```bash
cd ~/.claude/skills
git clone https://github.com/YOUR_USERNAME/strategic-analyst.git
```

### 前置要求

本 Skill 依赖 **Tavily** 进行深度研究级搜索。请在 Claude Code 的 `settings.json` 中配置 Tavily MCP：

```json
{
  "mcpServers": {
    "tavily": {
      "command": "npx",
      "args": ["-y", "tavily-mcp@0.1.4"],
      "env": {
        "TAVILY_API_KEY": "tvly-你的API密钥"
      }
    }
  }
}
```

如果没有 Tavily，系统会自动降级使用普通 WebSearch，但深度分析能力会有所下降。

### 激活方式

在 Claude Code 中输入以下任意一种请求即可激活：

- "帮我分析新能源汽车行业"
- "我想进入新茶饮市场，帮我评估一下机会"
- "这个 SaaS 赛道竞争格局怎么样？"
- "做一份关于 AI 硬件的战略分析报告"

---

## 使用示例

### 示例 1：市场进入决策

> "我想进入新茶饮行业，帮我分析一下市场机会和竞争格局"

Strategic Analyst 会：
1. 启动需求访谈，确认你的资源禀赋和进入方式
2. 调用 Tavily 搜索最新市场规模、主要玩家、融资动态
3. 应用波特五力、TAM-SAM-SOM、竞争格局、PESTEL 等框架
4. 输出一份包含数据溯源的完整战略分析报告

### 示例 2：投资决策支持

> "这个新能源电池项目值得投吗？帮我做个行业分析"

Strategic Analyst 会：
1. 识别你的投资人视角，侧重财务回报和风险评估
2. 搜索行业增长率、技术路线、政策风险、头部公司估值
3. 生成包含关键成功因素和投资建议的决策支持报告

### 示例 3：竞争策略制定

> "我们是做 B2B SaaS 的，最近竞争很激烈，该怎么定位？"

Strategic Analyst 会：
1. 聚焦 SaaS 行业的竞争格局和战略群组
2. 分析主要竞争对手的优劣势和定价策略
3. 给出差异化定位建议和防守/进攻策略

---

## 分析框架

| 框架 | 用途 |
|------|------|
| **波特五力模型** | 评估行业竞争强度和盈利能力 |
| **TAM-SAM-SOM** | 三层市场规模测算 |
| **竞争格局分析** | 市场集中度、战略群组、主要玩家画像 |
| **PESTEL 趋势分析** | 政治、经济、社会、技术、环境、法律宏观扫描 |
| **价值链分析** | 价值创造各环节和利润池分布 |
| **关键成功因素 (CSF)** | 识别行业关键能力要求和差距分析 |

---

## 数据透明度机制

我们深知战略分析中的数据质量至关重要。因此，本 Skill 强制要求：

| 数据类型 | 标识方式 | 可靠性 |
|---------|---------|--------|
| **直接引用数据** | 来源 + 发布时间 + 可信度星级 | ★★★★★ |
| **推算/估算数据** | 明确标注"估算"+ 计算公式 + 置信区间 | ★★★☆☆ |
| **行业共识数据** | 标注"经验值"+ 影响因素说明 | ★★☆☆☆ |

每份报告必含：
- ✅ 数据溯源章节
- ✅ 推算逻辑说明
- ✅ 时效性分布
- ✅ 数据缺口坦诚说明

---

## 输出示例

### 报告模板类型

1. **执行摘要版**：3-5 条核心结论 + 关键数据一览 + 建议行动
2. **学生学习版**：方法论讲解 + 理论案例结合 + 学习检查清单
3. **完整专业版**：8 大章节全面分析 + 详细数据支撑 + 附录

### HTML 报告特性

- 专业商务风格（深蓝主色调）
- 表格支持悬停下载 PNG/SVG
- 可信度星级颜色标注
- 响应式设计，支持打印

---

## 项目结构

```
strategic-analyst/
├── skill.yaml                    # Skill 配置
├── agent_instructions.md         # 智能体人设与边界
├── README.md                     # 本文件
├── frameworks/                   # 6 大分析框架模板
│   ├── industry_structure.md
│   ├── market_sizing.md
│   ├── competitive_landscape.md
│   ├── trend_analysis.md
│   ├── key_success_factors.md
│   └── value_chain.md
├── templates/                    # 报告模板
│   ├── executive_summary.md
│   ├── student_edition.md
│   ├── full_report.md
│   └── data_provenance.md
├── data_sources/                 # 数据源指南
│   ├── general.md
│   └── by_industry/
├── tools/                        # 工具脚本
│   ├── data_collector.py
│   ├── report_generator.py
│   └── quality_gate.py
├── checklists/                   # 检查清单
│   ├── pre_analysis.md
│   ├── data_collection.md
│   ├── quality_check.md
│   └── professional_boundaries.md
└── cases/                        # 分析案例
    └── new_tea_drinks_analysis.md
```

---

## 更新日志

### v0.3.0 (2026-03-29)
- HTML 表格支持悬停下载 PNG/SVG
- `data_collection.md` 成为强制中间产物
- 所有关键数据必须包含 `[来源](URL)` Markdown 链接

### v0.2.0 (2026-03-29)
- 新增 Tavily 深度搜索集成
- 新增多模态数据获取（PDF 提取、网页抓取、OCR 识别）
- 新增专业边界保持机制和质量门禁

### v0.1.0 (2026-03-29)
- 初始版本：6 大分析框架 + 3 种报告模板

---

## 许可证

CC BY-NC-SA 4.0

---

## 作者与交流


如果你：
- 对这个 Skill 的使用有任何问题
- 有新的分析框架想贡献
- 需要基于这个 Skill 的**定制化行业分析服务**

在微信公众号/小红书 搜索： 小王子和小企鹅

> **P.S.** 如果你正在寻找「AI 驱动的行业研究和战略分析服务」，欢迎私信交流。

---

*让每个创业者和投资人，都能拥有一个随身麦肯锡顾问。*
