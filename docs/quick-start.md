# 快速开始

> 适合第一次接触 OpenClaw 时快速上手。

## 推荐顺序

1. 安装并直接启动
2. 补齐环境变量
3. 知道配置和记忆文件放哪里
4. 学会先看日志再继续排查

## 1. 快速启动

```bash
# 直接启动
openclaw

# 指定配置文件
openclaw --config ~/.openclaw/config.yaml

# 调试模式
openclaw --debug
```

## 2. 环境变量配置

```bash
export OPENAI_API_KEY="sk-..."
export ANTHROPIC_API_KEY="sk-ant-..."
export OPENCLAW_LOG_LEVEL="debug"
```

## 3. 记忆文件管理

```bash
# 记忆文件位置
~/.openclaw/memory/

# 备份记忆
cp -r ~/.openclaw/memory/ ~/backup/
```

## 4. 基础日志查看

```bash
# 实时查看日志
tail -f ~/.openclaw/logs/openclaw.log

# 搜索错误
grep "ERROR" ~/.openclaw/logs/openclaw.log
```

## 快速参考

- 完整版技巧大全: [../openclaw-tips-complete.md](../openclaw-tips-complete.md)
- 进阶主题: [./advanced-and-performance.md](./advanced-and-performance.md)
- 问题排查: [./troubleshooting.md](./troubleshooting.md)
