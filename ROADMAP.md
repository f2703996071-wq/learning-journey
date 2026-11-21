# AI 辅助网站开发学习路线图

## 学习者画像
- **背景**：大一学生，Python 基础，MacBook Pro M1 Pro (16GB)
- **目标**：独立承接中小企业官网、外贸展示网站订单
- **工具栈**：Kilo + VS Code + GitHub + Next.js + shadcn/ui + Vercel + Cloudflare
- **现状**：无 HTML/CSS/JavaScript/React 基础

---

## 核心原则
1. **项目驱动**：每阶段产出可验证的实物成果
2. **AI 协作而非依赖**：用 Kilo 理解代码，而非单纯生成
3. **最小必要知识**：只学直接用于项目的知识
4. **循序渐进**：单次任务可在 1-2 周内完成

---

## 阶段规划概览

| 阶段 | 核心目标 | 预估周数 | 关键产出 |
|------|----------|----------|----------|
| 0 | 环境搭建与基础配置 | 1周 | 开发环境就绪，GitHub 仓库初始化 |
| 1 | Web 基础三件套 + React 入门 | 2-3周 | 一个静态个人简历页面 |
| 2 | Next.js 核心 + 组件化开发 | 2-3周 | 一个多页面博客/作品集网站 |
| 3 | shadcn/ui + 设计系统实战 | 2周 | 一个完整的企业官网 UI 原型 |
| 4 | 数据获取 + CMS + 部署上线 | 2-3周 | 个人网站正式上线，绑定自有域名 |
| 5 | 商业项目实战：企业官网 | 3-4周 | 可交付的中小企业官网模板 |
| 6 | 商业项目实战：外贸展示站 | 3-4周 | 多语言、SEO 优化的外贸网站 |
| 7 | 接单准备与作品集打磨 | 2周 | 完整作品集、报价体系、合同模板 |

---

## 详细阶段拆解

### 阶段 0：环境搭建与基础配置（第 1 周）

**学习目标**：
- 搭建专业开发环境
- 掌握 Git/GitHub 基础工作流
- 配置 Kilo 与 VS Code 集成
- 建立第一个项目仓库

**为什么先学这个**：
所有后续开发的基础设施，避免后期环境问题阻塞学习

**核心任务**：
1. 安装配置：Node.js (fnm/nvm)、pnpm、Git、VS Code 必装插件
2. GitHub 账号配置：SSH Key、GPG 签名、Profile 美化
3. Kilo 配置：API Key、权限设置、常用快捷键
4. 创建 `learning-journey` 单体仓库，包含：
   - `stage-0-setup/` 环境配置记录
   - `stage-1-web-basics/` 阶段 1 代码
   - ... 后续阶段以此类推
5. 学会：提交规范、分支策略、PR 流程

**完成标准**：
- [ ] `pnpm --version`、`node --version`、`git --version` 均正常输出
- [ ] GitHub 仓库 `learning-journey` 创建并推送首次提交
- [ ] Kilo 在 VS Code 中正常对话、读写文件
- [ ] 能独立完成：创建分支 → 修改代码 → 提交 → 推送 → 发起 PR

**Kilo 使用重点**：
- 让 Kilo 解释每条配置命令的作用
- 用 Kilo 生成 `.gitignore`、`.editorconfig`、commit message 模板
- 遇到报错先贴给 Kilo 分析，再尝试修复

---

### 阶段 1：Web 基础三件套 + React 入门（第 2-4 周）

**学习目标**：
- 理解 HTML 语义化、CSS 布局、JavaScript 核心语法
- 掌握 React 组件、Props、State、Hooks 基础
- 能阅读并修改简单的 React 组件代码

**为什么这个顺序**：
Next.js 本质是 React 框架，不懂 React 就无法理解 Next.js 的组件模型、生命周期、数据流

**核心任务**：

#### 1.1 HTML + CSS（3-4 天）
- 学习资源：MDN Web Docs 前 3 个模块 + 《CSS 权威指南》精选章节
- 实战：用 Kilo 克隆分析 [GitHub: html5-boilerplate](https://github.com/h5bp/html5-boilerplate) 理解标准模板
- 产出：语义化的单页简历 HTML（`stage-1-web-basics/resume.html`）

#### 1.2 CSS 布局进阶（3-4 天）
- Flexbox、Grid、响应式断点、CSS 变量
- 实战：用 Kilo 阅读 [GitHub: tailwindcss/tailwindcss](https://github.com/tailwindcss/tailwindcss) 核心源码理解原子化 CSS 思想
- 产出：简历页面响应式重构（移动端/平板/桌面端）

#### 1.3 JavaScript 核心（4-5 天）
- 重点：ES6+ 语法、异步编程、模块系统、DOM 操作基础
- 实战：用 Kilo 逐行解读 [GitHub: you-dont-need-jquery](https://github.com/you-dont-need/you-dont-need-jquery) 理解原生 JS 能力
- 产出：简历页面交互增强（平滑滚动、主题切换、技能条动画）

#### 1.4 React 入门（5-7 天）
- 核心概念：组件、JSX、Props、State、useEffect、useState、条件渲染、列表渲染
- 实战：用 Kilo 创建 Vite + React + TypeScript 项目，逐步将简历页面组件化
- 参考项目：[GitHub: reactjs/react.dev](https://github.com/reactjs/react.dev) 官方文档源码
- 产出：`stage-1-web-basics/resume-react/` 完整 React 版简历

**完成标准**：
- [ ] 能手写语义化 HTML 结构，不依赖 AI 生成
- [ ] 能用 Flex/Grid 实现任意两栏/三栏自适应布局
- [ ] 能解释 `async/await`、`Promise`、事件循环区别
- [ ] 能独立拆分 React 组件、管理 State、处理副作用
- [ ] 简历页面：语义化 HTML、响应式、主题切换、组件化拆分 ≥ 8 个组件

**Kilo 使用重点**：
- **读代码**：`@workspace` 读取项目文件，让 Kilo 解释组件树、数据流
- **改代码**：选中代码块 → Cmd+L → "帮我把这个类组件改成函数组件并加上 TypeScript 类型"
- **排错**：报错直接贴给 Kilo，先让它分析原因，再给修复建议
- **学概念**：遇到不懂的 Hook/语法，问 Kilo "用通俗例子解释 useEffect 依赖数组的作用"

---

### 阶段 2：Next.js 核心 + 组件化开发（第 5-7 周）

**学习目标**：
- 掌握 Next.js App Router：路由、布局、页面、加载状态、错误边界
- 理解服务端组件 (RSC) 与客户端组件的区别与协作
- 掌握数据获取：fetch、缓存、revalidate、SWR 模式
- 建立可复用的组件库雏形

**为什么这个顺序**：
Next.js 是生产级 React 框架，App Router 是新标准，RSC 模式改变了数据获取方式，必须系统掌握

**核心任务**：

#### 2.1 Next.js 项目初始化与路由系统（3-4 天）
- `pnpm create next-app@latest my-portfolio --typescript --tailwind --eslint --app --src-dir --import-alias "@/*"`
- 实战：用 Kilo 克隆阅读 [GitHub: vercel/next.js](https://github.com/vercel/next.js) 中的 `examples/` 目录理解最佳实践
- 产出：多路由结构（`/` 首页、`/about` 关于、`/projects` 作品、`/blog` 博客、`/contact` 联系）

#### 2.2 布局与元数据系统（2-3 天）
- `layout.tsx`、`page.tsx`、`loading.tsx`、`error.tsx`、`not-found.tsx`
- Metadata API：动态标题、描述、Open Graph、Twitter Card
- 产出：完整的 SEO 友好页面结构

#### 2.3 服务端组件与数据获取（4-5 天）
- RSC 默认服务端渲染、流式渲染、Suspense 边界
- `fetch` 扩展选项：`cache: 'force-cache' | 'no-store'`、 `next: { revalidate: 3600 }`
- 实战：用 Kilo 阅读 [GitHub: vercel/next-learn](https://github.com/vercel/next-learn) 课程代码
- 产出：博客列表页（SSG）、博客详情页（ISR）、项目展示页（SSR）

#### 2.4 客户端交互与组件库雏形（3-4 天）
- `"use client"` 指令、客户端组件边界设计
- 封装通用组件：Button、Card、Container、Section、Header、Footer
- 产出：`components/ui/` 目录下 ≥ 10 个可复用组件，有 Storybook 预览

**完成标准**：
- [ ] 能解释 RSC 与 Client Component 的区别、何时用哪个
- [ ] 能独立设计路由结构、配置 Metadata、处理加载/错误状态
- [ ] 能根据数据特性选择正确的缓存策略
- [ ] 作品集网站：5 个页面、响应式、SEO 完善、组件复用率 ≥ 60%
- [ ] 代码通过 `pnpm lint`、`pnpm typecheck`、`pnpm build` 无报错

**Kilo 使用重点**：
- 让 Kilo 生成路由结构骨架，自己填充业务逻辑
- 贴上 `layout.tsx` 让 Kilo 解释每个 export 的作用
- 数据获取报错时，让 Kilo 分析是缓存问题还是类型问题
- 组件封装时，让 Kilo 帮写 TypeScript 接口和 JSDoc 注释

---

### 阶段 3：shadcn/ui + 设计系统实战（第 8-9 周）

**学习目标**：
- 掌握 shadcn/ui "复制粘贴" 组件库的使用与定制
- 理解 Radix UI 原语、Tailwind CSS 配置、CSS 变量主题系统
- 建立属于自己的设计令牌、组件规范、文档站点

**为什么这个顺序**：
shadcn/ui 不是传统组件库，源码在你项目里，完全可控，适合学习组件设计原理并定制商业项目风格

**核心任务**：

#### 3.1 shadcn/ui 深度集成（3-4 天）
- `pnpm dlx shadcn@latest init` 配置 Tailwind、CSS 变量、路径别名
- 逐个安装所需组件：`button`、`card`、`dialog`、`form`、`table`、`dropdown-menu`、`toast`、`tooltip`、`avatar`、`badge`、`separator`、`skeleton`
- 实战：用 Kilo 阅读每个组件源码（`components/ui/button.tsx` 等），理解 `class-variance-authority` (cva) 模式
- 产出：组件库文档页面（`/ui-docs`）展示所有组件变体、状态、用法

#### 3.2 设计令牌与主题定制（3-4 天）
- 修改 `tailwind.config.ts`：颜色、字体、间距、圆角、阴影、断点
- CSS 变量方案：`--background`、`--foreground`、`--primary`、`--secondary`、`--muted`、`--accent`、`--destructive`、`--ring`
- 暗色模式：`class` 策略 + `next-themes` 实现系统跟随/手动切换/本地存储
- 实战：参考 [GitHub: shadcn-ui/ui](https://github.com/shadcn-ui/ui) 的 `apps/www` 理解官网设计系统
- 产出：完整的设计令牌文档、亮/暗两套配色、主题切换零闪烁

#### 3.3 企业官网 UI 原型构建（4-5 天）
- 页面规划：首页、关于我们、产品/服务、案例展示、新闻动态、联系我们
- 组件化拆解：Hero、FeatureGrid、TestimonialCarousel、PricingTable、ContactForm、Footer、Navbar
- 表单处理：React Hook Form + Zod 验证 + Server Action 提交
- 产出：`stage-3-enterprise-ui/` 完整企业官网静态原型，所有页面可交互、响应式、暗色模式正常

**完成标准**：
- [ ] 能解释 cva 原理，能基于 Radix UI 封装新组件
- [ ] 能独立配置 Tailwind 设计令牌，输出设计规范文档
- [ ] 暗色模式切换无闪烁、无布局偏移、持久化生效
- [ ] 企业官网原型：6 个页面、≥ 20 个组件实例、表单验证完整、Lighthouse 性能 ≥ 90
- [ ] 组件库发布为内部包（可选）：`pnpm publish --workspace` 到 GitHub Packages

**Kilo 使用重点**：
- 让 Kilo 批量安装 shadcn 组件并解释每个的依赖关系
- 贴上 `button.tsx` 让 Kilo 逐行解释 `cva`、`cn`、`forwardRef` 用法
- 修改 Tailwind 配置时，让 Kilo 生成配置并解释每个字段含义
- 遇到样式冲突，让 Kilo 分析 CSS 优先级、Tailwind 类名顺序问题

---

### 阶段 4：数据获取 + CMS + 部署上线（第 10-12 周）

**学习目标**：
- 掌握 Headless CMS（Contentlayer / Sanity / Notion API）集成
- 理解 Server Actions、表单处理、文件上传
- 完成 Vercel 部署、自定义域名绑定、Cloudflare DNS/CDN 配置
- 建立 CI/CD 流水线：Lint → TypeCheck → Build → Preview → Production

**为什么这个顺序**：
静态原型变成动态网站需要数据层；部署上线是交付的最后一公里，必须亲手走通

**核心任务**：

#### 4.1 CMS 集成与内容建模（4-5 天）
- 方案对比：Contentlayer (本地 MDX)、Sanity (实时协作)、Notion API (零成本)
- 推荐起步：Contentlayer + 本地 MDX 文件，零成本、类型安全、Git 管理内容
- 实战：用 Kilo 搭建 `content/` 目录结构、`contentlayer.config.ts`、Schema 定义
- 内容模型：BlogPost、Project、Service、TeamMember、Testimonial
- 产出：`lib/cms/` 完整数据获取层，类型安全的 `getPosts()`、`getProject()` 等函数

#### 4.2 Server Actions 与动态交互（3-4 天）
- 表单提交：联系表单、订阅邮件、询盘表单 → Server Action + Resend/SendGrid 发邮件
- 图片优化：`next/image` + Cloudflare Images / Vercel Blob / 本地 public
- 搜索功能：Algolia DocSearch / Meilisearch / 客户端 Fuse.js
- 产出：联系表单真实发邮件、博客全文搜索、图片自动 WebP/AVIF

#### 4.3 部署上线与域名配置（3-4 天）
- Vercel：连接 GitHub 仓库、环境变量配置、Preview Deployments
- Cloudflare：购买/转入域名、DNS 记录（CNAME www → cname.vercel-dns.com、A @ → 76.76.21.21）、SSL/TLS 设置、页面规则、Cache Rules
- 域名邮箱：Cloudflare Email Routing 或 Google Workspace / Zoho Mail
- 监控：Vercel Analytics、Speed Insights、Sentry 错误追踪
- 产出：`https://yourdomain.com` 正式上线，Lighthouse 全项 ≥ 90，Core Web Vitals 达标

**完成标准**：
- [ ] 能独立完成 CMS Schema 设计、内容增删改、前端类型安全获取
- [ ] 能编写 Server Action 处理表单、上传、邮件发送
- [ ] 个人网站正式上线：自有域名、HTTPS、CDN、邮箱、监控全配齐
- [ ] CI/CD：推送 main 分支自动部署生产环境，PR 自动生成 Preview 链接
- [ ] 文档化：`DEPLOYMENT.md` 记录部署架构、环境变量表、常见问题排查

**Kilo 使用重点**：
- 让 Kilo 生成 Contentlayer 配置、Schema 类型、获取函数模板
- Server Action 报错时，贴上错误堆栈让 Kilo 定位是序列化还是权限问题
- Vercel 部署失败时，贴上 Build Log 让 Kilo 分析是依赖缺失还是环境变量缺失
- Cloudflare DNS 配置截图给 Kilo，让它确认记录类型、代理状态是否正确

---

### 阶段 5：商业项目实战 - 中小企业官网（第 13-16 周）

**学习目标**：
- 完成一个可交付的企业官网标准化模板
- 掌握需求分析、原型设计、开发交付全流程
- 建立可复用的项目脚手架、组件库、部署脚本

**核心任务**：

#### 5.1 需求分析与原型设计（1 周）
- 标准企业官网页面清单：首页、关于、产品/服务列表、详情、新闻列表、详情、案例、联系、招聘、隐私政策、服务条款
- 线框图：Figma 绘制低保真原型，标注响应式断点、交互状态
- 内容结构：与客户确认文案、图片、视频素材规范
- 产出：`project-enterprise/requirements.md`、`project-enterprise/wireframes/`

#### 5.2 脚手架初始化与核心架构（1 周）
- 基于阶段 3-4 积累，创建 `create-enterprise-site` 脚手架
- 预置：TypeScript 严格模式、ESLint/Prettier、Husky、Commitlint、Tailwind 设计令牌、shadcn/ui 全套、CMS 层、Server Action 层、SEO 组件、Analytics、Sentry
- 产出：`project-enterprise/` 可一键初始化的标准项目

#### 5.3 页面开发与组件复用（2 周）
- 按原型逐页实现，复用率 ≥ 70%
- 重点难点：产品/服务多规格筛选、新闻分页加载、案例灯箱查看、多步骤联系表单
- 无障碍：语义化 HTML、ARIA 标签、键盘导航、颜色对比度、焦点可见
- 产出：所有页面完成功能开发、响应式测试通过

#### 5.4 质量保障与交付准备（1 周）
- 测试：单元测试、E2E 测试、视觉回归测试、Lighthouse CI
- 性能：Bundle 分析、图片优化、字体子集化、预加载关键资源
- SEO：Sitemap.xml、Robots.txt、结构化数据、Meta 标签完整性
- 文档：`README.md`、`DEPLOYMENT.md`、`CONTRIBUTING.md`、`CHANGELOG.md`
- 产出：可直接交付给客户的标准化项目包

**完成标准**：
- [ ] 拥有可复用的企业官网脚手架，新项目 30 分钟内跑通
- [ ] 完整企业官网：10+ 页面、CMS 可编辑所有内容、表单真实可用
- [ ] 质量门槛：TypeCheck 0 错误、Lint 0 警告、Build 成功、测试覆盖率 ≥ 80%
- [ ] 性能指标：LCP < 2.5s、CLS < 0.1、FID < 100ms、Lighthouse ≥ 95
- [ ] 交付包：源码 + 部署文档 + 后台使用手册 + 维护指南

**Kilo 使用重点**：
- 让 Kilo 生成脚手架模板文件、GitHub Actions 工作流、测试配置
- 开发中遇到复杂交互（如多级筛选），先让 Kilo 设计数据结构和状态管理方案
- 性能优化阶段，贴上 Bundle Analyzer 报告让 Kilo 提出优化建议
- 交付文档让 Kilo 根据代码自动生成 API 文档、组件用法示例

---

### 阶段 6：商业项目实战 - 外贸展示网站（第 17-20 周）

**学习目标**：
- 掌握国际化 (i18n) 路由、内容本地化、多货币/多语言切换
- 理解海外访问优化：CDN、边缘函数、字体加载、第三方脚本治理
- 掌握外贸 SEO：hreflang、Google Search Console、Schema.org 结构化数据

**核心任务**：

#### 6.1 国际化架构设计（1 周）
- Next.js App Router i18n：`[lang]` 路由段、Middleware 语言检测重定向
- 内容本地化策略：CMS 字段级翻译、路由级翻译、组件级翻译
- 语言切换器：URL 保持、SEO 友好、本地存储偏好
- 产出：`project-export/i18n-config.ts`、中英文双语内容模型

#### 6.2 海外性能优化（1 周）
- Vercel Edge Network / Cloudflare Workers 边缘中间件
- 字体策略：`next/font` 自托管 Google Fonts、变量字体、preload
- 第三方脚本：Google Analytics、Google Tag Manager、Crisp/Intercom 聊天、Trustpilot 徽章 → `next/script` 策略加载
- 图片：Cloudflare Images / ImageKit 全球 CDN、自动 WebP/AVIF、响应式尺寸
- 产出：海外节点 LCP < 2s、TTFB < 200ms

#### 6.3 外贸 SEO 与合规（1 周）
- `hreflang` 标签自动生成、Sitemap 多语言版本
- Schema.org：Organization、WebSite、Product、BreadcrumbList、FAQPage
- Google Search Console：站点地图提交、索引覆盖率监控、核心指标跟踪
- 合规：GDPR Cookie Banner、隐私政策多语言、服务条款、数据处理协议 (DPA)
- 产出：SEO 审计清单 100% 通过、合规页面上线

#### 6.4 询盘系统与转化优化（1 周）
- 询盘表单：多步骤、文件上传、reCAPTCHA v3、Server Action → 邮件 + CRM (HubSpot/Pipedrive) 双写
- 转化追踪：GA4 事件、GTM 数据层、热力图
- A/B 测试：Hero 文案、CTA 按钮、表单字段数量
- 产出：完整询盘闭环、转化漏斗可视化

**完成标准**：
- [ ] 双语网站：中英文完整内容、语言切换无刷新、URL 语义化
- [ ] 海外访问：美国/欧洲/东南亚节点测速达标
- [ ] SEO：Google 索引正常、hreflang 无报错、结构化数据验证通过
- [ ] 合规：Cookie Banner 符合 GDPR、隐私政策可访问
- [ ] 询盘：表单提交 → 邮件通知 + CRM 创建线索，端到端测试通过

**Kilo 使用重点**：
- 让 Kilo 生成 i18n 路由中间件、语言检测逻辑、翻译文件结构
- 贴上 Middleware 代码让 Kilo 解释 Edge Runtime 限制
- 结构化数据 JSON-LD 让 Kilo 根据 Schema.org 规范生成并验证
- 询盘表单 Server Action 让 Kilo 处理文件上传、验证、邮件模板、CRM API 对接

---

### 阶段 7：接单准备与作品集打磨（第 21-22 周）

**学习目标**：
- 建立专业作品集网站，展示真实项目案例
- 制定报价体系、合同模板、项目交付流程
- 掌握客户沟通、需求澄清、验收交付的实战技巧

**核心任务**：

#### 7.1 作品集网站建设（1 周）
- 项目案例页：背景挑战、技术方案、核心难点、解决方案、项目成果、客户评价
- 技术栈标签、项目链接、GitHub 仓库（脱敏版）、演示视频
- 关于我：技能树、学习历程、服务范围、联系方式
- 产出：`portfolio.yourdomain.com` 专业作品集上线

#### 7.2 商业文档体系（3-4 天）
- 报价单模板：基础套餐/进阶套餐/定制套餐、付费节点、维护费用
- 合同模板：项目范围、交付标准、验收条款、知识产权、保密条款、违约责任
- 需求问卷：项目背景、目标用户、功能清单、设计偏好、素材提供、时间节点
- 项目管理：Notion/Linear 模板、里程碑拆解、周报模板、验收清单
- 产出：`business-docs/` 完整文档包

#### 7.3 模拟接单实战（3-4 天）
- 在朋友/社区/Upwork/Fiverr 寻找 1-2 个低预算真实/模拟项目
- 完整走一遍：需求沟通 → 报价签约 → 原型确认 → 开发交付 → 验收收款 → 售后维护
- 复盘记录：耗时统计、坑点总结、流程优化、客户反馈
- 产出：至少 1 个真实商业交付记录、完整复盘文档

**完成标准**：
- [ ] 作品集网站专业、案例详实、联系转化路径顺畅
- [ ] 商业文档齐全、条款合规、可直接用于接单
- [ ] 完成至少 1 个端到端商业项目闭环（含收款）
- [ ] 能清晰向陌生人介绍：我做什么、怎么做、多少钱、为什么选我

**Kilo 使用重点**：
- 让 Kilo 根据项目代码自动生成案例页技术亮点描述
- 合同/报价模板让 Kilo 参考行业标准生成初版，再人工润色
- 模拟项目开发中，Kilo 作为结对程序员全程协作

---

## 学习节奏建议

| 时间投入 | 每周安排 | 关键动作 |
|----------|----------|----------|
| **全职/大量空闲** | 1 阶段/周 | 每天 4-6h，周末复盘总结 |
| **兼职/课余时间** | 1 阶段/2周 | 每天 1-2h，固定时间段，周末 4h 冲刺 |
| **碎片时间** | 1 阶段/3周 | 通勤看文档/视频，有电脑时写代码 |

**通用习惯**：
- 每天开始前：阅读今日任务、回顾昨日进度
- 编码时：遇到不懂先查文档/问 Kilo，再动手
- 每天结束：Git 提交、记录遇到的问题、明日计划
- 每周末：跑通所有测试、Lighthouse 审计、写周记总结

---

## 里程碑验收清单

| 里程碑 | 验收方式 | 通过标准 |
|--------|----------|----------|
| 环境就绪 | 运行验证脚本 | 所有版本号输出正常、Kilo 对话正常 |
| Web 基础 | 代码审查 + 口头解释 | 能不看代码解释组件树、数据流 |
| Next.js 掌握 | 新建一个微型项目 | 30分钟内搭建带路由、数据获取、部署的项目 |
| shadcn/ui 定制 | 现场封装一个新组件 | 基于 Radix UI 封装出带变体、TypeScript 的组件 |
| 个人网站上线 | 访问域名验证 | HTTPS、自有域名、CDN、监控全绿 |
| 企业官网模板 | 现场初始化新项目 | 5分钟跑通、10分钟改出新配色 |
| 外贸网站 | 海外节点测速 + SEO 审计 | 实测达标、Google Search Console 无报错 |
| 接单就绪 | 模拟客户面试 | 能流畅回答技术/流程/价格/交付问题 |

---

## 常见坑点预警

| 坑点 | 症状 | 预防/应对 |
|------|------|-----------|
| 依赖 AI 写代码不理解 | 代码跑通但改不了、排不了错 | **强制规则**：每次用 Kilo 生成/修改代码后，必须能逐行向自己解释 |
| 教程地狱 | 看完教程不会动手 | **只看官方文档 + 源码**，不看二手博客/视频教程 |
| 完美主义拖延 | 阶段 0 搭建环境花 2 周 | **时间盒**：每阶段设硬性截止日期，完不成也要进入下阶段 |
| 忽视基础 | 直接上 Next.js 不懂 React | **严守顺序**：阶段 1 不通过不进阶段 2 |
| 只重代码轻工程化 | 无测试、无 CI、无文档 | **每阶段必须有**：Lint、TypeCheck、Build、README 更新 |
| 孤军奋战不求助 | 卡在一个 Bug 一天 | **30分钟法则**：卡住 30min 必须问 Kilo/搜索/发 Issue |

---

## 起步行动清单（现在就做）

1. **克隆本计划到本地**：
   ```bash
   mkdir -p ~/learning-journey && cd ~/learning-journey
   git init
   # 将此文件保存为 ROADMAP.md
   ```

2. **阶段 0 第一个任务**：安装 fnm、Node.js 20 LTS、pnpm、Git
   ```bash
   brew install fnm git
   fnm install 20
   fnm use 20
   corepack enable pnpm
   ```

3. **配置 GitHub SSH**：
   ```bash
   ssh-keygen -t ed25519 -C "your@email.com"
   cat ~/.ssh/id_ed25519.pub  # 复制到 GitHub Settings → SSH Keys
   ```

4. **创建学习仓库并首推**：
   ```bash
   gh repo create learning-journey --private --source=. --push
   ```

5. **在 VS Code 安装 Kilo 扩展**，配置 API Key，测试对话

---

## 下一步

完成上述起步行动后，告诉我结果，我们正式开始**阶段 0**的详细学习任务。

---

*计划版本：v1.0 | 创建时间：2026-11-21 | 适用对象：大一学生、Python 基础、Mac M1 Pro*