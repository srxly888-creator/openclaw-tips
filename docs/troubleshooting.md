# 故障排查

> 遇到问题时，先看这里，再回完整指南深挖。

## 常见问题

### API Key 无效

```bash
openclaw --check-api-key
export OPENAI_API_KEY="new-key"
```

### 内存不足

```bash
openclaw --stats
openclaw --clear-cache
```

### 网络超时

```bash
export OPENCLAW_TIMEOUT=60000
export HTTP_PROXY=http://localhost:7890
```

## 日志分析

```bash
tail -f ~/.openclaw/logs/openclaw.log
grep "ERROR" ~/.openclaw/logs/openclaw.log
```

## 排查清单

- [ ] API Key 是否正确
- [ ] 网络是否正常
- [ ] 配置文件是否正确
- [ ] 依赖是否安装完整
- [ ] 当前用户是否具备所需权限
- [ ] 日志里是否已经给出直接错误原因

## 相关入口

- 完整版技巧大全: [../openclaw-tips-complete.md](../openclaw-tips-complete.md)
- 快速开始: [./quick-start.md](./quick-start.md)
