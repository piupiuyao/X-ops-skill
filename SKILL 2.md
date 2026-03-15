---
name: x-ops-v2
description: |
  X/Twitter growth system for founders. Three modules: Monitor (热点+舆论), Comment (评论引流), Post (内容生成).
  Works for 0-follower cold start AND established accounts.
  Requires OpenClaw with browser control (Chrome Relay).
  Triggers: "X运营", "发帖", "评论", "热点", "舆论监控", "tweet", "X post", "X comment", "grow twitter"
---

# X Ops v2 — Founder Growth System

专为 founder 设计的 X/Twitter 增长系统。基于 @MeredithCheng22 93天 0→244粉 的真实数据。

## 三大模块

| 模块 | 功能 | 触发词 |
|------|------|--------|
| **Monitor** | 热点新闻 + 舆论监控 + 竞品追踪 | "监控", "热点", "舆论" |
| **Comment** | Feed 浏览 + 高质量评论生成 | "评论", "互动", "comment" |
| **Post** | 内容生成 + 草稿管理 | "发帖", "写推", "post" |

---

## 🔴 Module 1: Monitor（监控）

### 1.1 执行流程

```
Step 1: Today's News（浏览器）
├── 导航到 x.com/explore/tabs/for-you
├── 抓取 "Today's News" 区块
├── 提取热点标题 + 帖子数量
└── 判断时效性（小时级）

Step 2: Google News 补充（浏览器）
├── 搜索 "AI marketing OR AI agent OR OpenAI OR Anthropic"
├── 筛选 24h 内新闻
└── 提取标题 + 来源

Step 3: 热点可蹭性评估
├── 相关度（1-5）：和你的产品/领域相关吗？
├── 时效性：还能蹭多久？（<6h/6-24h/24-48h）
├── 蹭法：QT/评论/借势发帖/观察不蹭
└── 账号匹配：个人号 vs 官方号
```

### 1.2 热点评估矩阵

| 类型 | 相关度 | 推荐动作 |
|------|--------|----------|
| 大厂发布（OpenAI/Anthropic/Google） | ⭐⭐⭐⭐⭐ | QT + 独特观点 |
| 行业融资/收购 | ⭐⭐⭐⭐ | 评论或借势发帖 |
| KOL 争议/热门讨论 | ⭐⭐⭐ | 评论（如果有独特视角） |
| 政策/监管 | ⭐⭐ | 观察为主 |
| 无关娱乐/政治 | ⭐ | 跳过 |

### 1.3 输出格式

```markdown
# 🔥 热点监控报告 | YYYY-MM-DD HH:MM

## Today's News（X 平台）
| 热点 | 帖子数 | 时效 | 相关度 | 蹭法 |
|------|--------|------|--------|------|
| ... | ... | ... | ... | ... |

## Google News（24h）
| 标题 | 来源 | 相关度 | 角度建议 |
|------|------|--------|----------|
| ... | ... | ... | ... |

## 📌 推荐行动
1. [热点A] — QT @xxx，角度：...
2. [热点B] — 借势发帖，切入点：...
```

---

## 🟡 Module 2: Comment（评论）

### 2.1 执行流程

```
Step 1: 浏览 Feed（浏览器）
├── 导航到 x.com/home
├── For You tab: 滚动抓取 10-15 条帖子
├── Following tab: 滚动抓取 10-15 条帖子
└── 提取：作者、内容、likes、comments、views、时间

Step 2: 筛选高质量帖子
├── 符合选帖标准（见下）
├── 话题相关（AI/Marketing/Founder/Startup）
└── 输出 5-10 条待评论

Step 3: 生成评论草稿
├── 每条帖子 1-2 个评论版本
├── 符合评论质量规则
└── 标注评论类型

Step 4: 用户审批 + 执行
├── 展示列表，等用户选择
├── 用户回复序号（如 1,3,5）
├── 浏览器执行，间隔 60s
└── 记录到 memory
```

### 2.2 选帖标准

**冷启动期（<500粉）：**
| 指标 | 推荐范围 | 原因 |
|------|----------|------|
| 原帖 views | 5K-50K | 有流量但不会被淹没 |
| 评论数 | <30 | 你的评论能被看到 |
| 发布时间 | <2小时 | 抢早期位置 |
| 作者粉丝 | 10K-100K | 中型 KOL 性价比最高 |

**成熟期（>1000粉）：**
| 指标 | 推荐范围 | 原因 |
|------|----------|------|
| 原帖 views | 10K-200K | 可以挑战更大流量 |
| 评论数 | <100 | 仍能被看到 |
| 发布时间 | <6小时 | 窗口可以更长 |
| 作者粉丝 | 50K-500K | 挑战大 KOL |

**绝对跳过：**
- views >500K（除非你是大V）
- 评论 >200 条
- 发布 >12小时
- 政治/争议话题

### 2.3 评论模板库

**Type A: 增量价值（最佳）**
```
We tested this at [公司] — [具体发现].
Key insight: [一句话总结].
```

**Type B: 数据补充**
```
Interesting. Our data shows [具体数字]% of [用户群] actually [行为].
The gap is [洞察].
```

**Type C: 反直觉**
```
Counterpoint: we found the opposite.
[具体例子]. Might be because [原因猜测].
```

**Type D: 问题延伸**
```
This makes me wonder: if [前提] is true, does [推论] follow?
We've seen [相关经验] but never connected the dots.
```

**Type E: Build in Public**
```
Going through this exact thing right now.
[具体情况]. Still figuring out [挑战].
```

### 2.4 评论禁用词

绝对不要用：
- "Great post!" / "Love this!"
- "So true!" / "This!"
- "Happy to help!"
- "DM me"
- 纯 emoji 回复
- "As a [身份], I think..."

### 2.5 输出格式

```markdown
# 💬 评论任务 | YYYY-MM-DD HH:MM

## 待评论帖子

### 1. @author_handle
**内容**: [帖子摘要]
**数据**: 👁️ 12K | ❤️ 234 | 💬 18 | ⏰ 45min ago
**链接**: https://x.com/...

**评论草稿 A** (增量价值):
> We tested this at Karis — found that X outperformed Y by 40%.
> The trick was focusing on [具体点].

**评论草稿 B** (问题延伸):
> This makes me wonder: if agents can do X, why are we still manually doing Y?

---

[更多帖子...]

---

## ⏳ 等待审批
回复序号执行评论（如: 1,3,5）
回复 "跳过" 取消
```

---

## 🟢 Module 3: Post（发帖）

### 3.1 账号阶段判断

| 阶段 | 粉丝数 | 策略重心 | 发帖频率 |
|------|--------|----------|----------|
| 冷启动 | 0-500 | 评论 70% + 发帖 30% | 1-2条/天 |
| 成长期 | 500-5K | 评论 50% + 发帖 50% | 2条/天 |
| 成熟期 | 5K+ | 发帖 70% + 评论 30% | 2-3条/天 |

### 3.2 内容类型矩阵

| 类型 | 效果排名 | 适合阶段 | 示例开头 |
|------|----------|----------|----------|
| **QT 热点** | ⭐⭐⭐⭐⭐ | 所有 | [Quote 热帖] + 独特角度 |
| **User Story** | ⭐⭐⭐⭐⭐ | 成长+ | "A customer just..." |
| **Data Drop** | ⭐⭐⭐⭐ | 所有 | "47% of founders..." |
| **Build in Public** | ⭐⭐⭐⭐ | 冷启动 | "Shipped X today. Here's what broke..." |
| **Contrarian** | ⭐⭐⭐⭐ | 成长+ | "Everyone says X. I think Y." |
| **Milestone** | ⭐⭐⭐ | 冷启动 | "Just hit 500 users!" |
| **Question** | ⭐⭐⭐ | 所有 | "Founders: how do you handle X?" |
| **Thread** | ⭐⭐⭐ | 成熟期 | "I analyzed 100 founder posts. Here's what I found:" |

### 3.3 Hook 公式（首行）

首行必须用以下之一：

1. **数字开头**: "47% of startups fail because..."
2. **对比/反直觉**: "Everyone says X. The data shows Y."
3. **情绪**: "Worst week of my startup life."
4. **问题**: "Why do 90% of AI tools feel the same?"
5. **大胆声明**: "Cold email is dead."
6. **故事开头**: "A customer just told me something wild."

### 3.4 长度规则

| 类型 | 字符限制 | 原因 |
|------|----------|------|
| Hot take | <100 | 越短越狠 |
| Standard | <150 | 不被折叠 |
| Story/Data | <220 | 需要展开 |
| Thread 每条 | <200 | 保持节奏 |

### 3.5 禁用词库

绝对不用：
- "We are excited/pleased/thrilled to announce"
- "Incredibly grateful"
- "Game-changer" / "Revolutionary"
- "Key takeaways" / "Let me break it down"
- "I've been thinking about..."
- "Unpopular opinion but..."
- "Hot take:" (用行动证明，不用标签)
- "🧵 Thread" (直接开始)
- 超过 2 个 emoji

### 3.6 发帖时间

**黄金时段（EST）：**
| 时段 | 效果 | 原因 |
|------|------|------|
| 8-10am | ⭐⭐⭐⭐⭐ | 美国早高峰 |
| 12-2pm | ⭐⭐⭐⭐ | 午休刷手机 |
| 5-7pm | ⭐⭐⭐ | 下班通勤 |

**黄金日：**
| 日期 | 效果 |
|------|------|
| 周二-周四 | 🔥🔥🔥 (10-15x 周末) |
| 周一/周五 | 🔥🔥 |
| 周六 | 🔥 (发 1 条轻内容) |
| 周日 | ❌ (休息) |

### 3.7 输出格式

```markdown
# ✍️ 发帖草稿 | YYYY-MM-DD

## 选题来源
- [ ] 今日热点
- [ ] 用户痛点库
- [ ] Build in Public
- [ ] 数据/洞察

## 草稿

### 版本 A (QT 热点)
> [Quote @xxx 的帖子]
> 
> This is exactly why we built Karis differently.
> Most AI tools wait for prompts. Ours monitors and acts.
> The shift from "assistant" to "agent" is everything.

**类型**: QT 热点
**字符**: 156
**Hook**: 对比型

---

### 版本 B (Build in Public)
> Shipped our new monitoring feature at 2am.
> Broke prod twice.
> Fixed it by 6am.
> 
> This is the founder life nobody talks about.

**类型**: Build in Public  
**字符**: 112
**Hook**: 故事型

---

## 📌 推荐
版本 A — 蹭今日热点，时效性强

## ⏳ 等待审批
回复 A/B 选择版本
回复 "改" + 反馈修改
```

---

## 执行命令

### 完整日常流程
```
用户: "跑一下 X 监控"

执行顺序:
1. Monitor — 热点 + 舆论
2. Comment — Feed 评论建议
3. Post — 基于热点生成草稿
4. 汇总报告 + 等待审批
```

### 单模块执行
```
"跑热点监控" → Module 1 only
"找评论机会" → Module 2 only  
"帮我写推" → Module 3 only
```

---

## 文件路径

```
~/Desktop/test/素材库/
├── 1-选题管理/
│   ├── 00-选题收集箱.md
│   ├── 01-待深化/
│   ├── 02-待发布/
│   └── 03-已发布/
├── 2-素材库/
│   ├── 用户痛点语言库.md
│   ├── 竞品内容.md
│   └── 金句库.md
└── 6-数据统计/
    └── 内容数据表.md
```

---

## 参考文档

- [references/data-evidence.md](references/data-evidence.md) — 93天数据证明
- [references/comment-templates.md](references/comment-templates.md) — 评论模板扩展
- [references/post-examples.md](references/post-examples.md) — 爆款帖子拆解
- [references/voice-guide.md](references/voice-guide.md) — 语气指南

---

*基于 @MeredithCheng22 真实数据构建 | 仅限 OpenClaw 使用*
