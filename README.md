# AFA DTC Skills

面向独立站与 DTC 品牌的全链路增长顾问 Skill 系统。30 个模块，三层架构，覆盖从市场洞察到规模化扩张的完整链路。

**最新版本：v2.4.6**

**作者**：1亿美刀站长阿发 · [小红书](https://xhslink.com/m/34JAVccyOdD) · [抖音](https://v.douyin.com/nSkhVHdGCrg/)

**所有内容开放，可以整套装，也可以只拿一部分。**

---

## 系统架构

AFA DTC Skills 不是一堆散装工具——它是一个三层架构的 AI 顾问系统：

```
                              ┌──────────┐
                         L0   │ afa(Hub) │   系统入口 · 一级路由 · 工作流编排
                              └────┬─────┘
                                   │
              ┌────────────────────┼────────────────────┐
              │                    │                    │
        ┌─────┴──────┐     ┌──────┴──────┐      ┌──────┴──────┐
   L1   │afa-diagnose│     │afa-dashboard│      │ 5×Supervisor │
        │ 全局诊断引擎│     │ 全局数据中枢 │      │              │
        └────────────┘     └─────────────┘      └──────┬───────┘
                                                       │
   L2                                          22 个 Worker 引擎
```

### 三层是什么意思？

| 层级 | 角色 | 做什么 |
|:---|:---|:---|
| **L0 Hub** | `afa` | 系统入口。接收用户请求，判断意图，路由到对的 Supervisor 或全局引擎。编排跨组工作流。 |
| **L1 Supervisor** | 5 个中枢 + 2 个全局引擎 | 二级路由。把 Hub 分配来的任务再派发给具体 Worker，协调多 Worker 串联，回收结果。 |
| **L2 Worker** | 22 个执行引擎 | 干活的。每个 Worker 专注一个领域，有自己的方法论、参考库和工作模式。 |

**关键规则**：Hub 不直接调用 Worker，Worker 不直接跨组调用其他 Worker。严格分层，越界请求走回交链路。

---

## 工具箱

### 🔀 Hub（系统入口）

| 模块 | 做什么 |
|:---|:---|
| `afa` | 主入口，一级路由器。接收任何 DTC 问题，自动路由到对的模块 |

### 🔍 全局引擎（直接向 Hub 汇报）

| 模块 | 做什么 |
|:---|:---|
| `afa-diagnose` | 全链路诊断与归因。"主治医师"——三阶段诊断法，8 大维度，输出行动处方 |
| `afa-dashboard` | 数据仪表盘与体检。三层看板，北极星指标追踪，异常预警 |

### 🏗️ afa-foundation — 品牌与产品基建中枢

| Worker | 做什么 |
|:---|:---|
| `afa-explore` | 用户洞察与市场探索。VOC 挖掘、市场机会评估、角度生成 |
| `afa-compete` | 竞争情报。竞争格局扫描、深度拆解、对标学习 |
| `afa-brand` | 品牌定位与识别。定位画布、声音架构、品牌故事、视觉识别 |
| `afa-product` | 产品策略。四维溢价评估、定价建模、产品组合优化 |
| `afa-launch` | 产品上市与冷启动。完整启动规划、PMF 评估、预算规划 |

### 💰 afa-paid — 付费获客中枢

| Worker | 做什么 |
|:---|:---|
| `afa-creative` | 创意生产与测试。视觉套件、脚本文案、Prompt Engineering、广告测试矩阵 |
| `afa-fb` | Meta 广告优化。账户结构、受众策略、创意文案、预算扩量、追踪归因 |
| `afa-gg` | Google Ads 优化。搜索广告、PMax、Shopping Feed、预算扩量 |
| `afa-tt` | TikTok 广告优化。账户设置、创意策略、TikTok Shop、联盟营销 |

### 🌱 afa-organic — 有机增长中枢

| Worker | 做什么 |
|:---|:---|
| `afa-seo` | SEO 与有机搜索增长。全面审计、关键词研究、页面优化、内容策略、链接建设 |
| `afa-social` | 社交内容与 UGC。全盘策略、UGC 项目、爆款脚本、社区飞轮 |
| `afa-influencer` | 网红与联盟营销。创作者筛选、触达合作、联盟计划、品牌大使 |
| `afa-pr` | 品牌公关与声誉管理。CPR 冷推、UGC 飞轮、危机响应、品牌保护 |
| `afa-geo` | AI 搜索可见度与本地化搜索。GEO/AEO 审计、引用机会挖掘 |

### 💎 afa-monetize — 变现与留存中枢

| Worker | 做什么 |
|:---|:---|
| `afa-convert` | 全链路转化率优化。审计、落地页优化、CRO 飞轮、结账优化 |
| `afa-cx` | 客户体验与服务智能。旅程映射、工单分析、情感分析、CX 自动化 |
| `afa-retain` | 用户留存与 LTV 增长。留存体检、生命周期管理、忠诚度、订阅防流失 |
| `afa-aov` | 客单价提升与利润优化。门槛设计、捆绑包、促销利润模拟、全链路 Upsell |
| `afa-email` | 邮件营销。自动化流设计、Campaign 文案、可交付性诊断、BFCM 作战 |
| `afa-sms` | SMS 营销。自动化流架构、对话式 SMS、跨渠道协同、频率治理 |

### 🚀 afa-scale — 运营与扩张中枢

| Worker | 做什么 |
|:---|:---|
| `afa-ops` | 运营与供应链优化。单位经济审计、库存管理、履约优化、团队架构 |
| `afa-expand` | 渠道扩张与多元化。渠道评估、Marketplace 入驻、批发、国际化、线下零售 |

---

## 工具路径图

### 预设工作流

AFA DTC Skills 内置 11 个预设工作流，覆盖从零起步到规模化的全阶段：

| # | 工作流 | 适用场景 | 执行链路 |
|:--|:---|:---|:---|
| 1 | **从零起步** | 什么都还没有 | explore → compete → brand → product → launch |
| 2 | **增长瓶颈突破** | 数据不好看，不知道卡在哪 | diagnose → 按 ICE 优先级执行 → dashboard 验证 |
| 3 | **广告体系搭建** | 要开始投广告了 | brand 确认 → creative → fb/gg/tt → convert 配合 |
| 4 | **留存体系搭建** | 复购太低，LTV 上不去 | retain → email → sms → aov |
| 5 | **内容营销体系** | 想做有机增长 | seo → geo → social → creative 配合 |
| 6 | **品牌升级** | 品牌老了，要重新定位 | compete → brand → creative + convert 配合 |
| 7 | **大促备战** | BFCM / 大促前准备 | product + creative → fb+gg+tt → convert+email+sms（三组并行） |
| 8 | **渠道扩展** | 想拓展新渠道 | expand 评估 → 按结果路由到对应 Supervisor |
| 9 | **紧急止血** | 现金流告急 | 按资产有无分支到 monetize/foundation/paid（多组联动） |
| 10 | **Level 0 引导** | 完全没方向 | 方向梳理 → explore → 进入从零起步 |
| 11 | **溢价能力构建** | 想提高利润率 | product 四维评估 → 按 Tier 路由到不同模块 |

### 常见路径

```
不知道做什么 → afa（Hub 自动路由）→ 对的模块

数据出问题 → afa-diagnose（诊断）→ 定位原因 → 对应 Worker 执行

从零开始 → afa-foundation → explore → compete → brand → product → launch

要投广告 → afa-paid → creative（素材）→ fb / gg / tt（投放）

做内容 → afa-organic → seo + social + influencer + pr

提高复购 → afa-monetize → retain + email + sms + aov

扩规模 → afa-scale → ops（运营）+ expand（渠道）
```

### 跨组协同

模块之间会自动协同。比如：

- 广告体系搭建时，`afa-paid` 会先拉 `afa-brand` 确认品牌定位，投放后拉 `afa-convert` 优化落地页
- 大促备战时，`foundation`、`paid`、`monetize` 三个 Supervisor 并行协同
- 任何模块遇到超出职责的请求，通过回交链路上报，Hub 重新路由——不会自作主张

---

## 数据流转

### Brand Brain — 模块间的数据总线

上游模块写入的文件自动成为下游模块的输入：

```
afa-explore → competitors.md（初步竞品）
    ↓
afa-compete → 更新 competitors.md（深化竞品分析）
    ↓
afa-brand → brand-master.md + voice-and-tone.md
    ↓
afa-product → products.md
    ↓
afa-launch → 上市计划（消费以上所有文件）
```

### Monetize 组协同规则

- email + sms 不同时触发同一事件（邮件先发 → 无响应 → SMS 跟进）
- `convert` 负责"第一次购买"，`retain` 负责"第二次及以后"
- `aov` 策略通过 `convert`（产品页）、`email`（交叉销售）、`cx`（购后追加）三个触点落地
- 每个 Worker 执行后关键指标变化回传 `learnings.jsonl`

---

## 模块全览

| # | 模块 | 层级 | 上级 | 工作模式 | 参考库文件 |
|:--|:---|:---|:---|:---|:---|
| 1 | afa | Hub | — | 11 预设工作流 | 5 |
| 2 | afa-diagnose | 全局引擎 | Hub | 5 种诊断模式 | 9 |
| 3 | afa-dashboard | 全局引擎 | Hub | 4 大工作流 | 9 |
| 4 | afa-foundation | Supervisor | Hub | 3 工作流 | — |
| 5 | afa-paid | Supervisor | Hub | 3 工作流 | — |
| 6 | afa-organic | Supervisor | Hub | 3 工作流 | — |
| 7 | afa-monetize | Supervisor | Hub | 4 工作流 | — |
| 8 | afa-scale | Supervisor | Hub | 3 工作流 | — |
| 9 | afa-explore | Worker | foundation | 4 种模式 | 11 |
| 10 | afa-compete | Worker | foundation | 4 种模式 | 11 |
| 11 | afa-brand | Worker | foundation | 6 种模式 | 12 |
| 12 | afa-product | Worker | foundation | 5 种模式 | 11 |
| 13 | afa-launch | Worker | foundation | 5 种模式 | 11 |
| 14 | afa-creative | Worker | paid | 5 种模式 | 16 |
| 15 | afa-fb | Worker | paid | 6 种模式 | 11 |
| 16 | afa-gg | Worker | paid | 5 种模式 | 12 |
| 17 | afa-tt | Worker | paid | 5 种模式 | 10 |
| 18 | afa-seo | Worker | organic | 6 种模式 | 13 |
| 19 | afa-social | Worker | organic | 6 种模式 | 11 |
| 20 | afa-influencer | Worker | organic | 6 种模式 | 11 |
| 21 | afa-pr | Worker | organic | 5 种模式 | 9 |
| 22 | afa-geo | Worker | organic | 4 种类型 | 9 |
| 23 | afa-convert | Worker | monetize | 6 种类型 | 10 |
| 24 | afa-cx | Worker | monetize | 6 种模式 | 11 |
| 25 | afa-retain | Worker | monetize | 5 种模式 | 11 |
| 26 | afa-aov | Worker | monetize | 5 种模式 | 12 |
| 27 | afa-email | Worker | monetize | 4 种模式 | 10 |
| 28 | afa-sms | Worker | monetize | 6 种类型 | 10 |
| 29 | afa-ops | Worker | scale | 8 种模式 | 10 |
| 30 | afa-expand | Worker | scale | 6 种模式 | 12 |

---

## 如何安装

### Claude Code

```shell
claude plugin marketplace add afadtc/afa-dtc-skills
```

### 通用方式（Claude Code / Codex）

```shell
npx skills add afadtc/afa-dtc-skills
```

### 手动安装

```shell
git clone https://github.com/afadtc/afa-dtc-skills.git
```

将 `skills/` 目录下的模块复制到你的项目中即可使用。

---

## 如何更新

### Claude Code 插件市场

```shell
claude plugin marketplace update afa-dtc-skills
```

### npx 方式

重新运行安装命令即可，安装和更新用同一条命令：

```shell
npx skills add afadtc/afa-dtc-skills
```

---

## 目录结构

```
afa-dtc-skills/
├── afa/                        # Hub — 系统入口与工作流编排
│   ├── SKILL.md
│   ├── _system/                # 系统级规则（路由、交接、铁律等）
│   └── references/             # 路由清单、诊断规则、案例库等
│
├── afa-diagnose/               # 全局诊断引擎
├── afa-dashboard/              # 全局数据中枢
│
├── afa-foundation/             # Supervisor: 品牌与产品基建
│   └── Workers:
│       ├── afa-explore/        #   市场探索
│       ├── afa-compete/        #   竞争情报
│       ├── afa-brand/          #   品牌定位
│       ├── afa-product/        #   产品策略
│       └── afa-launch/         #   产品上市
│
├── afa-paid/                   # Supervisor: 付费获客
│   └── Workers:
│       ├── afa-creative/       #   创意生产
│       ├── afa-fb/             #   Meta 广告
│       ├── afa-gg/             #   Google Ads
│       └── afa-tt/             #   TikTok 广告
│
├── afa-organic/                # Supervisor: 有机增长
│   └── Workers:
│       ├── afa-seo/            #   SEO
│       ├── afa-social/         #   社交内容
│       ├── afa-influencer/     #   网红营销
│       ├── afa-pr/             #   品牌公关
│       └── afa-geo/            #   AI 搜索可见度
│
├── afa-monetize/               # Supervisor: 变现与留存
│   └── Workers:
│       ├── afa-convert/        #   转化率优化
│       ├── afa-cx/             #   客户体验
│       ├── afa-retain/         #   用户留存
│       ├── afa-aov/            #   客单价提升
│       ├── afa-email/          #   邮件营销
│       └── afa-sms/            #   SMS 营销
│
├── afa-scale/                  # Supervisor: 运营与扩张
│   └── Workers:
│       ├── afa-ops/            #   运营优化
│       └── afa-expand/         #   渠道扩张
│
├── LICENSE
└── README.md
```

每个 Worker 模块包含：
- `SKILL.md` — 模块定义、工作模式、执行规则
- `references/` — 方法论框架、案例库、模板、基准数据

---

## 许可证

本项目采用 [CC BY-NC 4.0](LICENSE) 许可证。

- **个人使用、学习、研究、非商业项目**：不需要署名，不需要申请
- **公开发布衍生作品**（文章、工具、课程等）：请注明来源
- **商业用途**：需要单独授权，请联系作者
