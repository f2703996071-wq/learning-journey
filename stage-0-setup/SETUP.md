# 阶段 0：环境搭建与基础配置 - 完成记录

## 完成时间
2026-11-21

## 环境版本
- Node.js: v20.18.0
- npm: 10.8.2
- pnpm: 12.21.0
- Git: 2.50.1 (Apple Git-155)

## 安装路径
- Node.js: `~/.local/node/`
- pnpm: `~/.local/node/bin/pnpm`
- 全局包目录: `~/.local/share/pnpm/`

## Shell 配置 (已添加到 ~/.zshrc)
```bash
export PATH="$HOME/.local/node/bin:$PATH"
```

## Git 配置
```bash
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
git config --global init.defaultBranch main
git config --global core.editor "code --wait"
git config --global commit.template ~/.gitmessage
```

## SSH Key 生成与 GitHub 配置
```bash
# 生成 Ed25519 SSH Key
ssh-keygen -t ed25519 -C "你的邮箱"

# 启动 ssh-agent 并添加密钥
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# 复制公钥到剪贴板
cat ~/.ssh/id_ed25519.pub | pbcopy
```
然后在 GitHub Settings → SSH and GPG keys → New SSH key 粘贴。

## 仓库初始化
```bash
mkdir -p ~/learning-journey && cd ~/learning-journey
git init
# 创建目录结构
mkdir -p stage-0-setup stage-1-web-basics stage-2-nextjs stage-3-shadcn-ui stage-4-cms-deploy stage-5-enterprise stage-6-export stage-7-freelance
# 复制路线图
cp /path/to/ROADMAP.md .
# 添加配置文件
# .gitignore, .editorconfig, .gitmessage
git add .
git commit -m "chore: init learning-journey repository with stage structure"
```

## VS Code 推荐插件
在 VS Code 扩展市场搜索并安装：
- **Kilo** (AI 编程助手)
- **ESLint** (代码检查)
- **Prettier** (代码格式化)
- **Tailwind CSS IntelliSense** (Tailwind 智能提示)
- **TypeScript Vue Plugin (Volar)** (TypeScript 支持)
- **GitLens** (Git 增强)
- **Error Lens** (行内错误显示)
- **Auto Rename Tag** (HTML 标签自动重命名)
- **Path Intellisense** (路径补全)

## Kilo 配置
1. VS Code 中打开 Kilo 扩展
2. 配置 API Key（在 Kilo 设置中）
3. 测试对话：在 Kilo 聊天面板输入 "你好" 验证连接

## 验证清单
- [x] `node --version` 输出 v20.18.0
- [x] `pnpm --version` 输出 12.21.0
- [x] `git --version` 输出 2.50.1
- [x] GitHub SSH Key 配置完成
- [x] 仓库 `learning-journey` 创建并首次提交
- [x] Kilo 在 VS Code 中正常对话
- [x] 能独立完成：创建分支 → 修改 → 提交 → 推送 → PR

## 下一步
进入**阶段 1：Web 基础三件套 + React 入门**
- 目录：`~/learning-journey/stage-1-web-basics/`
- 第一个任务：创建语义化 HTML 简历页面- 练习 Git 工作流完成于 2026-11-22
