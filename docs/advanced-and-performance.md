# 高级与性能

> 适合已经能跑起来、想进一步把 OpenClaw 用顺手的人。

## 高级用法

### 自定义 Prompt

```yaml
prompts:
  system: |
    你是一个专业的 AI 助手。
    请使用简洁、专业的语言回答。
```

### 多模型切换

```bash
openclaw --model gpt-4o
export OPENCLAW_DEFAULT_MODEL="claude-3-5-sonnet-20241022"
```

### 技能链组合

```text
search -> analyze -> report
```

## 性能优化

### 缓存策略

```javascript
const openclaw = new OpenClaw({
  cache: {
    enabled: true,
    ttl: 3600,
    maxSize: 1000
  }
});
```

### 并发控制

```javascript
const openclaw = new OpenClaw({
  concurrency: {
    maxConcurrent: 5,
    queueSize: 100
  }
});
```

### 速度优化

```javascript
await openclaw.prewarm();
openclaw.chat({ message: "Hello", stream: true });
```

## 最佳实践

- 每个 Skill 尽量保持单一职责。
- 配置、技能和团队约定尽量放进版本控制。
- 先做缓存和并发限制，再做更复杂的优化。
- 排查性能问题时优先看日志和可重复复现的场景。

## 继续阅读

- 完整版技巧大全: [../openclaw-tips-complete.md](../openclaw-tips-complete.md)
- 故障排查: [./troubleshooting.md](./troubleshooting.md)
- 实战案例: [./cases-and-resources.md](./cases-and-resources.md)
