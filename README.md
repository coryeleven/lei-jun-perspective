# 雷军 · 思维操作系统

一个基于公开信息蒸馏的雷军视角 Skill：用来分析商业机会、创业决策、产品定位、品牌表达和组织取舍。

它不是雷军本人，也不代表雷军或小米官方观点。它的目标是把雷军公开言论和历史决策中反复出现的思维方式，整理成一个可调用的「思维顾问」。

## 能力概览

- **6 个核心心智模型**：顺势而为、群众路线、效率信仰、认知突破驱动、面子-里子双层决策、示弱即力量。
- **7 条决策启发式**：从超级用户、第一把扳手、公开承诺、拥抱自嘲、亲自接管等角度辅助判断。
- **表达 DNA**：短句、口语化、示弱、金句收尾、精确数字、故事化表达。
- **事实边界**：遇到最新事实、财报、事故、交付量、监管许可等问题时，要求先核验来源，不把过期资料包装成实时事实。
- **诚实边界**：不冒充本人，不代替真实人物做私下意图判断、政治表态、投资建议或官方承诺。

## 安装

### Codex

将仓库安装到 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/coryeleven/lei-jun-perspective.git ~/.codex/skills/lei-jun-perspective
```

重启 Codex 后生效。

更新到最新版：

```bash
cd ~/.codex/skills/lei-jun-perspective
git pull
```

### Claude / 兼容 Skills 目录

如果你的环境使用项目级 `.claude/skills/`：

```bash
mkdir -p .claude/skills
git clone https://github.com/coryeleven/lei-jun-perspective.git .claude/skills/lei-jun-perspective
```

也可以下载 ZIP 后解压，确保目录结构为：

```text
skills/
└── lei-jun-perspective/
    ├── SKILL.md
    ├── README.md
    ├── references/
    └── scripts/
```

## 使用方式

在对话中说以下任意表达即可触发：

- `用雷军的视角分析这个决策`
- `雷军会怎么看这个产品定位`
- `切换到雷军`
- `如果雷总来做，会怎么拆`
- `Lei Jun perspective`
- `Xiaomi founder mindset`

示例：

```text
用雷军的视角，分析我们要不要进入 AI 硬件赛道。
```

```text
雷军会怎么看这次产品定价？请同时考虑性价比和高端化的矛盾。
```

```text
切换到雷军，帮我 review 这份发布会叙事。
```

退出角色：

```text
退出角色
切回正常
不用扮演了
```

## 适合的问题

- 创业方向、赛道选择、商业模式判断
- 产品定位、定价、发布会叙事、品牌表达
- 用户参与、社区运营、口碑增长
- 高端化与性价比之间的取舍
- 创始人个人 IP、示弱表达、危机沟通
- 用公开材料分析雷军或小米相关商业决策

## 不适合的问题

- 纯代码审查、技术选型细节
- 需要雷军本人授权或私下想法的问题
- 政治表态、监管立场、法律承诺
- 实时股价、最新事故、最新交付量等未核验事实
- 医疗、法律、金融投资等高风险建议

## 事实核验规则

这个 Skill 会尽量区分三类内容：

1. **公开事实**：来自演讲、公告、财报、访谈、权威报道。
2. **解释框架**：例如「面子-里子双层决策」「示弱即力量」，属于基于公开材料的分析，不是已证实心理事实。
3. **近期待核验线索**：例如最新财报、事故、交付量、工厂投产、监管许可，只能作为搜索入口，回答前需要重新核验。

近期待核验线索见：

- [`references/latest-facts.md`](references/latest-facts.md)

事实一致性验证报告见：

- [`references/fact-validation-2026-06-11.md`](references/fact-validation-2026-06-11.md)

## 文件结构

```text
lei-jun-perspective/
├── SKILL.md                         # 核心 Skill：触发规则、心智模型、工作流、表达 DNA
├── README.md                        # 安装与使用说明
├── references/
│   ├── latest-facts.md              # 近期待核验事实线索
│   ├── fact-validation-2026-06-11.md # 事实一致性验证报告
│   └── research/                    # 6 维度调研笔记
│       ├── 01-writings.md
│       ├── 02-conversations.md
│       ├── 03-expression-dna.md
│       ├── 04-external-views.md
│       ├── 05-decisions.md
│       └── 06-timeline.md
└── scripts/
    ├── quality_check.py             # Skill 质量检查
    ├── merge_research.py
    ├── download_subtitles.sh
    └── srt_to_transcript.py
```

## 验证

运行质量检查：

```bash
python3 scripts/quality_check.py SKILL.md
```

当前版本检查结果：`6/6 PASS`。

## 更新日志

- **2026-06-11**：优化角色边界、事实核验规则和安装说明；新增近期待核验事实线索与事实一致性验证报告。
- **2026-06-10**：首次蒸馏，信息截止日期 2026-06-10。

## 声明

本 Skill 由 [女娲 · Skill造人术](https://github.com/alchaincyf/nuwa-skill) 生成，并经后续事实边界与安装说明优化。内容基于公开信息提炼，非雷军本人授权，非小米官方材料，仅供思维拓展、学习和分析参考。

创建者：[花叔](https://x.com/AlchainHust)
