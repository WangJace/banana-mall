# Banana Mall 🍌

> AI-powered e-commerce detail page generation & editing workspace  
> AI 电商详情页生成与编辑工作台

---

## ✨ Overview / 项目简介

Banana Mall is an AI-native workspace designed to turn product images into fully structured, high-conversion e-commerce detail pages.

Banana Mall 是一个 AI 原生的电商内容工作台，可以将商品图片转化为完整的高转化详情页。

---

<img width="3840" height="2029" alt="image" src="https://github.com/user-attachments/assets/8f197875-61f3-4513-a8f6-a162f5d245bf" />
<img width="3840" height="2029" alt="image" src="https://github.com/user-attachments/assets/43315a12-2e32-4db2-a366-43f1dfebec2e" />
<img width="3840" height="2029" alt="image" src="https://github.com/user-attachments/assets/697186df-51a4-4fd1-bfc5-425f9fca6dd7" />





## 🧠 What You Can Do / 核心能力

- 🖼️ Upload product images and analyze product information  
  上传商品图片，自动解析产品信息

- ✍️ Generate structured detail pages with AI  
  使用 AI 生成结构化电商详情页

- 🧩 Edit and regenerate sections flexibly  
  支持模块级编辑与重生成

- 🔌 Connect any OpenAI-compatible API  
  支持接入任意 OpenAI-compatible API

- 🧪 Multi-model support (Gemini / OpenAI / custom providers)  
  支持多模型（Gemini / OpenAI / 自定义模型）

- 💻 Run as Web app or Desktop app  
  支持 Web 与桌面端运行

---

## 📸 Demo / 示例展示

> Place your screenshots or demo images below  
> 在此处放置你的演示截图或效果图

### 🧩 Detail Page Editor / 编辑器界面
![editor-demo](./docs/images/editor-demo.png)

### 🧠 AI Product Analysis / AI 商品分析
![analysis-demo](./docs/images/analysis-demo.png)

### 📦 Generated Result / 生成结果
![export-demo](./docs/images/export-demo.png)

> Create these image files:  
> 请在项目中创建以下图片路径：

```
docs/images/editor-demo.png
docs/images/analysis-demo.png
docs/images/export-demo.png
```

---

## 🚀 Quick Start / 快速开始

```bash
npm install
npm run prisma:generate
npm run prisma:migrate
npm run dev
```

Then open the local address printed by Next.js.  
请打开 Next.js 启动后输出的本地访问地址。

---

## 🔑 Environment / 环境变量

Create `.env` based on `.env.example`:

基于 `.env.example` 创建 `.env` 文件：

```env
OPENAI_API_KEY=
OPENAI_BASE_URL=
DATABASE_URL=
```

Supports any OpenAI-compatible API.  
支持任意 OpenAI-compatible API（包括代理或自建服务）。

---

## 🏗 Architecture / 技术架构

- Next.js (App Router)
- Prisma (Database)
- OpenAI-compatible API layer
- Modular AI pipeline (analysis / planning / generation)
- Electron (Desktop build)

---

## 💻 Web + Desktop / Web 与桌面端

### Web

```bash
npm run dev
npm run build && npm run start
```

### Desktop (Windows EXE)

```bash
npm run build:desktop
npm run dist:win
```

Web 与 Desktop 共用同一套业务逻辑：

> Electron + Next standalone + electron-builder

---

## 🧩 Core Features / 核心功能

### 1. AI Product Analysis / 商品分析
- Extract structured product data  
  提取结构化商品信息
- Generate selling points and descriptions  
  自动生成卖点与文案

### 2. Detail Page Generation / 详情页生成
- Multi-section layout generation  
  多模块详情页结构生成
- AI-generated copy and image prompts  
  AI 文案与图片提示词生成

### 3. Section Editing System / 模块编辑系统
- Regenerate individual sections  
  支持单模块重生成
- Version control for sections  
  模块版本管理

### 4. Provider System / 模型接入系统
- OpenAI-compatible API support  
  支持 OpenAI-compatible API
- Dynamic model discovery  
  动态模型发现
- Multi-provider switching  
  多模型切换

---

## 📦 Project Structure / 项目结构

```
app/            # Next.js App Router
components/     # UI components
lib/            # AI / services / utils
prisma/         # database schema
desktop/        # electron entry
scripts/        # build scripts
```

---

## ⚠️ Notes / 注意事项

- Logs, storage, and local DB are ignored in git  
  日志、存储数据、本地数据库不会提交到 git

- `.env` is not committed  
  `.env` 文件不会被提交

- Designed for local-first development  
  以本地开发为优先设计

---

## 📖 Docs / 文档

- 中文文档: [README.zh-CN.md](./README.zh-CN.md)  
- English Docs: [README.en.md](./README.en.md)

---

## 🧠 Vision / 项目愿景

> Turn ideas into products, instantly.  
> 让想法，直接变成商品。

---

## 📌 Roadmap / 发展规划

- [ ] Template system / 模板系统  
- [ ] Multi-user collaboration / 多人协作  
- [ ] Plugin ecosystem / 插件生态  
- [ ] API service layer / API 服务化  
- [ ] Cloud version / 云端版本  

---

## 🤝 Contributing / 贡献

PRs are welcome.  
欢迎提交 PR。

---

## ⭐ Support / 支持

If you like this project, give it a star ⭐  
如果你觉得这个项目不错，欢迎点个 Star ⭐
