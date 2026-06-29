# NasaVPN 博客 — CLAUDE.md

Jekyll 静态博客，托管于 GitHub Pages（`matosrf506-gif.github.io`），为 NasaVPN 产品提供多语言内容营销。

---

## 一、Git 身份（最高红线）

**每次提交前必须验证 repo 级别的 git 身份，绝不能用全局身份暴露个人信息。**

```bash
# 验证（必做）
git config --local user.email
git config --local user.name

# 若未设置，执行：
git config --local user.email "matosrf506-gif@users.noreply.github.com"
git config --local user.name "matosrf506-gif"

# SSH 推送
git push origin main   # remote 已配置为 github-matosrf506:matosrf506-gif/matosrf506-gif.github.io.git
```

全局 git config 含个人真实身份（Bamboo742 / Jim），**绝不能出现在此仓库的任何提交中**。

---

## 二、产品定位（核心！写文章必读）

**NasaVPN** — 跨境专用网络加速器

| 核心卖点 | 描述 |
|---------|------|
| **跨境专用** | 专为跨境业务、AI办公、出海电商设计 |
| **独享固定原生住宅IP** | 来自真实 ISP 的住宅 IP，一人独享，固定不变 |
| **全球纯净节点** | 私有节点，非共享数据中心，99.9% 稳定在线 |
| **全平台支持** | Windows / macOS / iOS / Android / 路由器 |

官网：`https://www.nasavpn.com/`

### 写文章时的产品描述规范

**✅ 正确描述（必须使用）**
- 跨境专用网络加速器
- 独享固定原生住宅 IP（强调：来自真实 ISP，非数据中心）
- 全球纯净节点
- 稳定访问 ChatGPT / Claude / Netflix（不说"翻墙"）
- 出海业务稳定直连

**❌ 错误描述（禁止使用）**
- ~~独享节点（NasaVPN 不主打节点，主打 IP）~~
- ~~消除 CAPTCHA（不夸大功效）~~
- ~~梯子、翻墙、科学上网、FQ~~（合规用词）
- ~~VPN~~（正式文案用"网络加速器"，标签/SEO 可用 VPN）

**产品核心逻辑**：数据中心 IP（共享池）→ 平台识别为代理 → CAPTCHA/封号风险。NasaVPN 提供原生住宅 IP（来自真实 ISP）→ 平台视为普通用户 → 稳定接入。

---

## 三、提交规范

```
<type>: <简短描述>

feat     新文章、新功能
fix      修复 bug、修正内容
chore    配置变更
refactor 重构
docs     文档
perf     性能优化
ci       CI/CD
```

示例：
```
feat: add Vietnamese post — dedicated IP for ChatGPT
fix: correct product positioning in streaming article
chore: update IndexNow workflow key
```

---

## 四、文章写作规范

### 4.1 文件命名

```
# 中文文章
_posts/YYYY-MM-DD-{slug}.md

# 小语种文章
_posts/YYYY-MM-DD-{lang}-{slug}.md

# 示例
_posts/2026-06-28-ai-zhang-hao-wei-he-xu-yao-zhuan-shu-ip.md   # zh
_posts/2026-06-29-vi-nasavpn-ip-rieng-chatgpt.md               # vi
_posts/2026-06-29-en-nasavpn-dedicated-ip-guide.md             # en
```

### 4.2 Front Matter 模板

```yaml
---
title: "文章标题"
date: YYYY-MM-DD HH:MM:SS +0800
categories: [分类]
tags: [标签1, 标签2, 标签3]
lang: zh                    # zh / en / vi / ja / ko / tr
excerpt: "一句话摘要，显示在文章卡片，100字以内"
description: "SEO描述，160字以内，含主关键词"
image: /assets/images/covers/dedicated-ip.svg
---
```

### 4.3 可用封面图

| 文件 | 适用话题 |
|------|---------|
| `dedicated-ip.svg` | 独享IP / 账号安全 / 核心产品介绍 |
| `chatgpt.svg` | ChatGPT / Claude / AI 工具接入 |
| `streaming.svg` | Netflix / Disney+ / 流媒体 |
| `en-chatgpt.svg` | 英文版 ChatGPT 话题 |
| `intro.svg` | 产品综合介绍 |

### 4.4 分类参考

| 适用场景 | 中文 | 英文 | 越南语 | 日语 | 韩语 |
|---------|------|------|-------|------|------|
| 电商/账号 | 跨境工具 | Cross-Border | Công Cụ Xuyên Biên | 越境ツール | 해외 도구 |
| AI工具 | AI加速 | AI Tools | Công Cụ AI | AI活用 | AI 도구 |
| 流媒体 | 流媒体 | Streaming | Streaming | ストリーミング | 스트리밍 |
| 开发者 | 开发者工具 | Dev Tools | Công Cụ Dev | 開発者向け | 개발 도구 |

### 4.5 内容要求

- 字数：中文 1000–1800 字，小语种 700–1200 字
- 文章角度必须围绕**独享固定原生住宅 IP** 的价值（非通用 VPN 话题）
- 结构：痛点场景 → 原因分析（共享 IP 的问题）→ NasaVPN 解决方案 → 实操/对比 → CTA
- 必须包含：对比表格（数据中心 IP vs 住宅 IP）、blockquote CTA
- CTA 格式：`> 🚀 **[立即试用 NasaVPN](https://www.nasavpn.com/zh/)** — 独享固定原生住宅 IP，稳定访问 ChatGPT / Claude / Netflix`

---

## 五、多语言结构

| 语言 | 目录 | lang 值 |
|------|------|--------|
| 中文（默认） | `/` | zh |
| 英文 | `/en/` | en |
| 越南语 | `/vi/` | vi |
| 日语 | `/ja/` | ja |
| 韩语 | `/ko/` | ko |
| 土耳其语 | `/tr/` | tr |

### 首页 Hero Banner（`_layouts/home.html`）

Hero 内联 SVG，通过 Liquid 变量根据 `page.lang` 自动切换 5 个文本：

```liquid
h_sublabel   # Logo 下方副标签，如 "博客 · AI加速 · 流媒体解锁"
h_tagline    # 中央主标语，如 "专属 IP · 私有节点 · 稳定在线"
h_pill1      # 功能药丸1，如 "ChatGPT 加速"
h_pill2      # 功能药丸2，如 "Claude 稳定连接"
h_pill3      # 功能药丸3，如 "Netflix 4K 加速"
```

底部状态栏（`Connected — US West · Dedicated IP · Latency 38ms`）固定英文，不需要翻译。

---

## 六、项目结构

```
matosrf506-gif.github.io/
├── _layouts/
│   ├── default.html     # 页面框架：head / header（含语言切换）/ footer
│   ├── home.html        # 首页：Hero SVG（语言联动）+ 文章列表
│   ├── post.html        # 文章页：双栏 + 侧边栏 CTA（含产品介绍）
│   └── page.html / category.html
├── _posts/              # 所有文章（中文 + 小语种）
├── _data/
│   └── navigation.yml   # 6 种语言导航菜单
├── assets/
│   ├── css/style.css    # 全站样式
│   ├── images/
│   │   ├── covers/      # 文章封面图
│   │   ├── nasavpn-logo.png   # 站点 Logo（header + favicon + 侧边栏 CTA）
│   │   └── site-header.svg    # （已废弃，Hero 已改为内联 SVG）
│   └── js/lazy-load.js
├── en/ vi/ ja/ ko/ tr/  # 各语言子目录（index.html + category/）
├── about/
├── index.html           # 中文首页
├── _config.yml
├── BingSiteAuth.xml     # 必应站长验证（key: C7AC7A203979CD8726931D22B6249A9E）
├── C7AC7A203979CD8726931D22B6249A9E.txt   # IndexNow 密钥文件
└── .github/workflows/indexnow.yml         # 自动提交 IndexNow
```

### 侧边栏 CTA（`_layouts/post.html`）

已实现多语言：NasaVPN Logo + 产品介绍 Tagline + 3 个特性条目 + 下载按钮。修改时注意同步 6 种语言版本。

---

## 七、SEO

- hreflang 已在 `default.html` 配置（6 种语言）
- Bing 站长工具已验证（`BingSiteAuth.xml`）
- IndexNow 自动提交：推送 `_posts/**` 时触发，host: `matosrf506-gif.github.io`
- 关键词重点：`NasaVPN`、`独享IP`、`原生住宅IP`、`ChatGPT加速`、`跨境加速器`
