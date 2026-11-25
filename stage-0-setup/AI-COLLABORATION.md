# AI 协作规范

## 1. Prompt 模板

### 新功能开发
背景：[业务场景，如：企业官网需要产品详情页] 需求：[具体功能点，越具体越好] 约束：[技术栈、现有组件、性能预算、无障碍要求] 验收：[如何验证功能完成]


### Bug 修复
现象：[复现步骤、预期 vs 实际] 怀疑原因：[你的判断] 最小复现：[相关代码片段或文件路径] 验收：[修复后如何验证]


### 代码重构
目标：[重构目的：性能/可读性/复用/类型安全] 范围：[涉及文件/组件] 保持：[不变的行为/接口] 验收：[测试通过、Lighthouse 不降、类型无报错]


## 2. Code Review 检查清单

- [ ] 语义化 HTML 正确（header/nav/main/section/article/aside/footer）
- [ ] 无障碍：alt、aria-label、键盘可达、颜色对比度
- [ ] SEO：Meta 完整、结构化数据、hreflang（多语言）
- [ ] TypeScript：无 any、类型收窄正确、接口复用
- [ ] React：组件单一职责、Props 接口清晰、副作用在 useEffect
- [ ] Next.js：RSC/Client Component 边界正确、缓存策略匹配业务
- [ ] 性能：无巨大 Bundle、图片优化、字体自托管、脚本策略加载
- [ ] 安全：无敏感信息泄露、CSP、外部链接 noopener
- [ ] 测试：关键路径有测试、Lighthouse ≥ 95

## 3. 验收标准模板

| 功能 | 验收方式 | 通过标准 |
|------|----------|----------|
| 页面渲染 | 浏览器访问 / Playwright | 无 JS 报错、布局不崩、内容完整 |
| 响应式 | DevTools 设备工具栏 | 320px/768px/1024px/1440px 均正常 |
| 无障碍 | axe-core / Lighthouse | 无严重/中等问题、AA 级通过 |
| SEO | Lighthouse / 手动检查 | Meta/结构化数据/Sitemap 完整 |
| 表单 | 真实提交 | 验证生效、邮件/CRM 收到、成功反馈 |
| 部署 | Vercel Preview / Production | Build 通过、环境变量生效、域名解析正常 |
