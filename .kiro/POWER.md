# Superpowers for Kiro

Superpowers 是一个完整的软件开发工作流系统，为你的编码助手提供一套可组合的"技能"。

## 概述

Superpowers 提供了一套经过验证的开发工作流程和最佳实践，包括：

- **测试驱动开发 (TDD)** - 先写测试，始终如一
- **系统化调试** - 基于流程而非猜测
- **协作模式** - 头脑风暴、计划编写、代码审查
- **复杂度降低** - 以简洁为首要目标

## 工作流程

1. **brainstorming** - 在编写代码前激活。通过提问细化粗略想法，探索替代方案，分段展示设计以供验证。保存设计文档。

2. **using-git-worktrees** - 设计批准后激活。在新分支上创建隔离工作区，运行项目设置，验证干净的测试基线。

3. **writing-plans** - 有了批准的设计后激活。将工作分解为小任务（每个 2-5 分钟）。每个任务都有确切的文件路径、完整代码和验证步骤。

4. **subagent-driven-development** 或 **executing-plans** - 有了计划后激活。为每个任务分派新的子代理并进行两阶段审查（规格合规性，然后代码质量），或分批执行并设置人工检查点。

5. **test-driven-development** - 实现期间激活。强制执行 RED-GREEN-REFACTOR：编写失败测试，观察失败，编写最小代码，观察通过，提交。删除在测试之前编写的代码。

6. **requesting-code-review** - 任务之间激活。根据计划审查，按严重程度报告问题。关键问题会阻止进度。

7. **finishing-a-development-branch** - 任务完成时激活。验证测试，展示选项（合并/PR/保留/丢弃），清理工作树。

## 可用技能

### 测试
- **test-driven-development** - RED-GREEN-REFACTOR 循环（包含测试反模式参考）
- **verification-before-completion** - 确保问题真正修复

### 调试
- **systematic-debugging** - 4 阶段根因分析流程（包含根因追踪、纵深防御、基于条件的等待技术）

### 协作
- **brainstorming** - 苏格拉底式设计细化
- **writing-plans** - 详细实现计划
- **executing-plans** - 带检查点的批量执行
- **dispatching-parallel-agents** - 并发子代理工作流
- **requesting-code-review** - 预审查清单
- **receiving-code-review** - 响应反馈
- **using-git-worktrees** - 并行开发分支
- **finishing-a-development-branch** - 合并/PR 决策工作流
- **subagent-driven-development** - 快速迭代与两阶段审查（规格合规性，然后代码质量）

### 元技能
- **writing-skills** - 遵循最佳实践创建新技能（包含测试方法）
- **using-superpowers** - 技能系统介绍

## 使用方法

技能会根据上下文自动激活。你不需要做任何特殊操作，只需正常与 Kiro 交互即可。

例如：
- 当你开始构建新功能时，brainstorming 技能会自动激活
- 当你需要调试问题时，systematic-debugging 技能会自动激活
- 当你准备实现时，test-driven-development 技能会自动激活

## 技能文件位置

所有技能文件位于 `skills/` 目录下，每个技能都有自己的子目录和 `SKILL.md` 文件。

## 哲学

- **测试驱动开发** - 先写测试，始终如一
- **系统化而非临时** - 流程优于猜测
- **降低复杂度** - 简洁是首要目标
- **证据而非声明** - 在宣布成功之前先验证

## 更多信息

- **主页**: https://github.com/obra/superpowers
- **问题反馈**: https://github.com/obra/superpowers/issues
- **博客文章**: https://blog.fsck.com/2025/10/09/superpowers/

## 许可证

MIT License
