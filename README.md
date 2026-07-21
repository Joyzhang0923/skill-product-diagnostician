# Skill Product Diagnostician

把 AI Skill 当作产品，而不只是一段 prompt 来诊断。

`skill-product-diagnostician` 会先判断用户的真实目的，再通过预执行侦察、六维评分和证据分级，拆解、比较或优化一个 AI Skill，并给出最高优先级的行动建议。

## 能做什么

- **学习设计逻辑**：完整拆解一个 Skill，提炼可迁移的方法，而不是简单复述功能。
- **优化自己的 Skill**：定位最弱的 1–2 个维度，给出 Before/After 和三步行动计划。
- **购买判断**：根据定位、产品结构、定价和替代方案，给出明确结论。
- **竞品对比**：使用同一任务、同一证据标准横向比较多个 Skill。
- **先体验再分析**：目标可安全运行时，先测试主流程，再进行评分。
- **证据分级**：严格区分实测、资料可见、推断和信息不足。

## 六维诊断框架

| 维度 | 核心问题 |
|---|---|
| 定位精准度 | 为谁解决什么高价值问题，为什么选它？ |
| 产品结构设计 | 输入多省事、流程多聪明、输出多可用？ |
| 包装与呈现 | 用户能否快速看懂、感兴趣并建立信任？ |
| 定价与商业化 | 价格如何锚定价值，商业模式能否持续？ |
| 迭代成熟度 | 是否经过真实使用打磨，未来能否进化？ |
| 推广与冷启动 | 用户在哪里，如何触达、信任和传播？ |

每个评分都必须附证据与置信度。信息不足时不使用“中间分”掩盖未知。

## 安装

```bash
git clone https://github.com/Joyzhang0923/skill-product-diagnostician.git
cp -R skill-product-diagnostician/skill-product-diagnostician ~/.codex/skills/
```

重新打开 Codex 会话后即可使用。

## 使用示例

```text
使用 $skill-product-diagnostician 拆解这个 Skill，告诉我最值得学习的三个设计。
```

```text
使用 $skill-product-diagnostician 诊断我的本地 Skill，找出最该改的三个地方。
```

```text
使用 $skill-product-diagnostician 比较 A 和 B。请用相同任务实测，并给出场景化推荐。
```

```text
这个 Skill 值得买吗？请核验当前价格，说明适合谁、不适合谁。
```

## 证据标签

- `✅ 实测`：真正调用目标 Skill，并获得了用户可见输出。
- `📄 资料可见`：来自可复核文件、产品页或公开材料。
- `🔍 推断`：根据已有证据作出的解释，不能冒充事实。
- `⚪ 信息不足`：当前证据无法支持判断。

静态阅读或模拟推演不能标记为实测。

## 仓库结构

```text
skill-product-diagnostician/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── report-templates.md
    └── rubric.md
```

## 隐私与安全

- 诊断产品体验，不公开复述目标 Skill 的私密 prompt。
- 不擅自安装未知 Skill、购买产品、登录账号或执行外部副作用操作。
- 不编造价格、销量、评价、版本历史或内部实现。

## License

[MIT](LICENSE)
