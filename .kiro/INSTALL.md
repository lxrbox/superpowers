# 在 Kiro 中安装 Superpowers

## 前提条件

- 已安装 Kiro
- 已安装 Git

## 安装步骤

### 方法 1: 从 Git 仓库安装（推荐）

1. 克隆 Superpowers 仓库到 Kiro Powers 目录：

```bash
mkdir -p ~/.kiro/powers
git clone https://github.com/obra/superpowers.git ~/.kiro/powers/superpowers
```

2. 重启 Kiro 或重新加载 Powers

Power 将自动被 Kiro 发现并加载。

### 方法 2: 手动安装

1. 下载项目：

```bash
cd ~/.kiro/powers
git clone https://github.com/obra/superpowers.git
```

2. 验证文件结构：

确保以下文件存在：
- `~/.kiro/powers/superpowers/POWER.md`
- `~/.kiro/powers/superpowers/power.json`
- `~/.kiro/powers/superpowers/skills/` 目录

3. 重启 Kiro

## 验证安装

启动 Kiro 并询问：

```
你有 superpowers 吗？
```

或者尝试触发一个技能：

```
帮我规划这个功能
```

如果安装成功，brainstorming 技能应该会自动激活。

## 使用方法

### 自动激活

技能会根据上下文自动激活。例如：

- 当你说"帮我规划..."时，brainstorming 技能会激活
- 当你说"帮我调试..."时，systematic-debugging 技能会激活
- 当你开始实现时，test-driven-development 技能会激活

### 手动加载技能

如果需要手动加载特定技能，可以使用 Kiro 的 steering 文件系统：

```
加载 writing-skills 技能
```

### 可用技能列表

所有技能位于 `skills/` 目录下：

- `brainstorming` - 头脑风暴和设计
- `test-driven-development` - 测试驱动开发
- `systematic-debugging` - 系统化调试
- `writing-plans` - 编写实现计划
- `executing-plans` - 执行计划
- `subagent-driven-development` - 子代理驱动开发
- `requesting-code-review` - 请求代码审查
- `receiving-code-review` - 接收代码审查
- `using-git-worktrees` - 使用 Git 工作树
- `finishing-a-development-branch` - 完成开发分支
- `verification-before-completion` - 完成前验证
- `dispatching-parallel-agents` - 分派并行代理
- `writing-skills` - 编写新技能
- `using-superpowers` - Superpowers 介绍

## 更新

更新到最新版本：

```bash
cd ~/.kiro/powers/superpowers
git pull
```

然后重启 Kiro 或重新加载 Powers。

## 故障排除

### Power 未加载

1. 检查文件是否存在：
   ```bash
   ls -la ~/.kiro/powers/superpowers/POWER.md
   ls -la ~/.kiro/powers/superpowers/power.json
   ```

2. 检查 Kiro 日志中的错误信息

3. 确保 JSON 文件格式正确：
   ```bash
   cat ~/.kiro/powers/superpowers/power.json | python -m json.tool
   ```

### 技能未激活

1. 确认 Power 已正确加载
2. 尝试明确请求技能："使用 brainstorming 技能"
3. 检查 `power.json` 中的 steering 配置

### 与其他 Powers 冲突

如果与其他 Powers 有冲突，可以：

1. 调整 `power.json` 中的 `inclusion` 设置
2. 将某些技能设置为 `manual` 而非 `auto`
3. 在项目级别覆盖配置

## 项目级别配置

在项目中创建 `.kiro/steering/` 目录，可以添加项目特定的技能或覆盖 Superpowers 的行为。

## 获取帮助

- **问题反馈**: https://github.com/obra/superpowers/issues
- **完整文档**: https://github.com/obra/superpowers
- **博客文章**: https://blog.fsck.com/2025/10/09/superpowers/

## 许可证

MIT License - 详见 LICENSE 文件
