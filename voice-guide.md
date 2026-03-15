# 声音匹配指南

## 一、为什么声音匹配很重要

X 上的账号声誉建立在一致性上。如果你的帖子/评论有时候像一个分析师，有时候像一个朋友，有时候像一个营销人员，读者不会有"我知道这个人是谁"的感觉，不会建立真正的关注意愿。

AI 生成内容最常见的失败：**生成的内容质量还行，但不像这个人写的。**

---

## 二、声音指纹：四个维度

### 维度 1：句子节奏

**短句风格（50-80字符/句）：**
- 特征：每句话都能独立成立。不解释，只陈述。
- 示例：
  ```
  Shipped at 2am. Broke prod by 3am. Fixed by 6am.
  This is the part nobody talks about.
  ```
- 识别方式：帖子里经常有单行句，很少有"because"或"which means"

**中句风格（80-120字符/句）：**
- 特征：有因果，但不啰嗦。
- 示例：
  ```
  Most AI tools fail not because the AI is bad, but because
  nobody uses them after the first week.
  ```

**长句风格（>120字符/句）：**
- 特征：喜欢展开论述，带转折和修饰。
- 示例：
  ```
  The reason most founder-led sales fail isn't product fit —
  it's that founders are too close to the problem to notice
  when a customer is being polite instead of interested.
  ```

**匹配规则**：
- 如果账号是短句风格 → 生成内容中不要出现超过 100 字符的长句
- 如果账号是长句风格 → 不要强行切成短句，会失去原有的"深思熟虑"感

---

### 维度 2：语气类型

**干货型**：
- 特征：直接给结论/建议，不带情绪，读起来像备忘录
- 识别词：数字、步骤、"The key is"、"What works is"
- 示例账号特征：帖子里大量列表，很少感叹号
- 匹配要求：避免感叹号，避免情绪词，每句话必须有信息量

**故事型**：
- 特征：先给场景，再给结论，读起来像在讲话
- 识别词："I was", "We found", "A customer told me", 时间词（"last week", "3 months ago"）
- 匹配要求：有场景设定，有具体细节，有情绪转折

**观点型**：
- 特征：强烈的立场，喜欢用"I think", "I believe"，有时会挑衅
- 识别词："The real reason", "Nobody talks about", "The honest truth is"
- 匹配要求：必须有明确立场，避免中立模糊的表达

**互动型**：
- 特征：喜欢问问题，引发讨论，帖子结尾常有问句
- 识别词："What's your take?", "Am I wrong?", "Curious what you think"
- 匹配要求：内容必须有讨论入口，不能只是陈述

---

### 维度 3：Emoji 使用

| 风格 | 描述 | 匹配规则 |
|------|------|----------|
| **完全不用** | 0 emoji | 生成内容中不加任何 emoji |
| **偶尔（功能性）** | 只用来标注列表或区分段落（→ ✅ ❌ 等） | 只在标注用途时加，不加情绪 emoji |
| **常用（情绪性）** | 🔥💡🚀 等情绪表达 | 可以加，但控制在 1-2 个 |

**重要**：如果账号从不用 emoji，但你生成的内容里加了 → 立刻暴露是 AI 写的。

---

### 维度 4：标志性表达

每个账号都有自己习惯的词汇和句式。提取这些，在生成内容时引用。

**提取方法**：
- 读最近 20 条帖子，圈出重复出现的词或句式
- 记录他们不用的词（比如从不说"leverage"，从不用"ecosystem"）

**示例：**
- 账号 A 喜欢说 "the real problem is..." / "nobody talks about..."
- 账号 B 喜欢用数字列表，每条 <10 个词
- 账号 C 每条帖子最后都有一个问句

---

## 三、声音匹配检查流程

生成帖子或评论后，对照以下清单：

```
□ 句子长度符合账号习惯？（短/中/长）
□ 语气类型匹配？（干货/故事/观点/互动）
□ Emoji 使用符合账号风格？
□ 有没有用到账号的标志性词汇/句式？
□ 有没有用了账号从不用的词？（如 "thrilled", "excited to share"）
□ 读出来，像这个人说的话吗？
```

---

## 四、常见 AI 腔识别（必须避免）

以下表达是 AI 生成内容的典型特征，任何账号都不该出现：

**结构性 AI 腔：**
- "Let me break this down..."
- "Here are 5 key takeaways:"
- "At the end of the day..."
- "It's worth noting that..."
- "This is a nuanced topic, but..."

**情绪性 AI 腔：**
- "I'm incredibly grateful/humbled/excited"
- "This resonates deeply"
- "What an insightful post"
- "Thrilled to announce"

**观点性 AI 腔：**
- "There are valid points on both sides"
- "It's complex and multifaceted"
- "As we navigate this evolving landscape"
- 任何无立场的中性陈述（AI 怕得罪人）

**格式性 AI 腔：**
- 回复里用 **加粗** 强调词（真人不这么写评论）
- 过度使用分号
- 每段结尾都有总结句

---

## 五、新账号（无历史帖子）的处理

如果账号是新号，没有历史帖子来提取声音指纹：

**Step 1：询问用户以下问题**

```
1. 你平时说话是简洁干脆型，还是喜欢展开解释型？
2. 你更倾向于分享数据/方法，还是分享故事/经历？
3. 你愿意在帖子里表达强烈立场，还是更倾向中立分析？
4. 你用 emoji 吗？用哪些？
5. 给我看 2-3 个你觉得"这个人写得好"的账号，你喜欢他们什么？
```

**Step 2：根据回答建立初始声音档案**

**Step 3：发帖后更新**

第一批帖子发出去，看哪些表现好（互动率高）→ 强化那种风格
第一批帖子发出去，看哪些表现差 → 分析原因，调整声音档案

---

## 六、Tier 1 vs Tier 2 的声音侧重

**Tier 1 (0-500)：真实感 > 完美**

- 不要过度打磨，太精致的帖子反而不像真人
- 允许"不完整"的想法（"Still figuring this out"）
- 故事型和 Build in Public 类内容里，可以有轻微的不确定感
- 这个阶段最重要的声音特征：**真实**

**Tier 2 (500-2000)：一致性 > 完美**

- 开始建立"这个账号有固定风格"的认知
- 每条帖子都要过声音检查
- 在 niche 内要显得有权威感 → 更少不确定语气，更多明确立场
- 这个阶段最重要的声音特征：**一致**
