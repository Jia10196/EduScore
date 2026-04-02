# ✍ EduScore — 智能英语写作提升系统

<div align="center">

![EduScore](https://img.shields.io/badge/EduScore-V1.0-2563EB?style=for-the-badge&logo=bookstack&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML5-Single%20File-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![AI Powered](https://img.shields.io/badge/AI-Powered-8B5CF6?style=for-the-badge&logo=openai&logoColor=white)

**AI 驱动的英语写作批改工具，支持四六级 · 雅思 · 托福评分标准**

[🚀 立即使用](#快速开始) · [📖 用户手册](#文档) · [🔧 部署指南](#部署) · [❓ 常见问题](#常见问题)

</div>

---

## ✨ 功能特性

| 模块 | 功能说明 |
|------|---------|
| ✏️ **语法诊断** | 识别 47 种语法错误类型（时态、主谓一致、冠词、介词等），附中文修改建议 |
| 📚 **词汇升级** | 检测基础词汇，结合考试类型推荐 5-8 条高阶替换词，含适用度评分与例句 |
| 🔄 **句式改写** | 提供长句简化、短句合并、主被动转换、强调句、倒装句等 6 种改写建议 |
| 📊 **结构分析** | 逐段评析引言/正文/结尾，评估过渡词使用质量与段落连贯性（满分 10 分） |
| 🎯 **AI 评分** | 从语法、词汇、句式、结构四维度给出百分制评分，输出 Top 3 提分建议 |

### 支持的考试类型

- 🇨🇳 **四级 CET-4**（425-710 分）
- 🇨🇳 **六级 CET-6**（425-710 分）
- 🌏 **雅思 IELTS**（1-9 分）
- 🌏 **托福 TOEFL**（0-30 分）

---

## 🚀 快速开始

### 方式一：直接打开（最简单）

下载 `index.html`，用浏览器打开即可使用。

> ⚠️ 本地文件模式下浏览器会阻止跨域请求，建议使用方式二或三。

### 方式二：本地服务器

```bash
# Python（推荐）
python -m http.server 8000
# 然后访问 http://localhost:8000

# 或使用 Node.js
npx serve .
```

### 方式三：部署到 GitHub Pages（推荐）

1. Fork 本仓库
2. 进入仓库 **Settings → Pages**
3. Source 选择 `main` 分支，目录选择 `/root`
4. 保存后，访问 `https://your-username.github.io/eduscore`

---

## 🔑 API 配置

系统需要调用大语言模型 API 进行智能分析，支持以下提供商：

| 提供商 | 费用 | 国内访问 | 推荐指数 |
|--------|------|----------|---------|
| [Groq](https://console.groq.com) | 🟢 完全免费 | 需科学上网 | ⭐⭐⭐⭐⭐ |
| [硅基流动](https://siliconflow.cn) | 🟢 免费额度 | ✅ 直接访问 | ⭐⭐⭐⭐ |
| [OpenRouter](https://openrouter.ai) | 🟡 极低成本 | 需科学上网 | ⭐⭐⭐ |
| 自定义 | 自定 | 取决于服务 | ⭐⭐⭐ |

### 用户自行配置

点击页面右上角 **⚙ 设置** → 选择提供商 → 填入 API Key → 测试连接 → 保存。

### 管理员内置 Key（供所有用户使用）

编辑 `index.html`，找到以下代码并填入你的 Key：

```javascript
const BUILTIN_PROVIDER = 'groq';   // 提供商
const BUILTIN_KEY = '';             // ← 填入你的 API Key
```

---

## 📁 项目结构

```
eduscore/
└── index.html          # 完整应用（单文件，无需其他依赖）
```

本项目为纯前端单页应用，所有功能包含在一个 HTML 文件中，无需后端服务器，无需安装任何依赖。

---

## 🖥️ 技术栈

- **前端框架**：原生 HTML5 + CSS3 + JavaScript（ES6+），无第三方框架
- **UI 设计**：响应式深色主题，支持桌面端与移动端
- **AI 接口**：兼容 OpenAI API 格式，支持多家 LLM 提供商
- **字体**：DM Sans · Noto Sans SC · JetBrains Mono（Google Fonts）

---

## 📖 文档

- [用户操作手册（Word）](./docs/EduScore_用户操作手册_V1.0.docx)

---

## 🌐 浏览器兼容性

| 浏览器 | 最低版本 |
|--------|---------|
| Google Chrome | 90+ |
| Microsoft Edge | 90+ |
| Firefox | 88+ |
| Safari | 14+ |

---

## ❓ 常见问题

**Q：状态显示「未配置 Key」，无法分析？**
A：请按照上方 API 配置步骤操作，或联系管理员确认是否已内置 Key。

**Q：分析需要多久？**
A：通常 30-60 秒。系统需依次调用 5 次 AI 接口，网络状况会影响速度。

**Q：提示「请求太频繁」？**
A：免费 API 有速率限制，请等待约 1 分钟后重试。

**Q：更换设备后需要重新配置 API Key 吗？**
A：是的，Key 保存在浏览器本地，不同设备需分别配置。

**Q：支持中文作文批改吗？**
A：当前版本专注英语写作，暂不支持中文。

---

## 📄 License

MIT License © 2025 EduScore

---

<div align="center">
  <sub>如有问题或建议，欢迎提交 <a href="../../issues">Issue</a> 或 <a href="../../pulls">Pull Request</a></sub>
</div>
