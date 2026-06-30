# MxPage

MxPage is an AI-native workspace for generating and editing e-commerce product detail pages and Xiaohongshu image posts.

MxPage 是由灵矩绘境出品并维护的 AI 商品图文工作台，面向电商详情页、小红书图文、批量商品页面生成和本地私有化部署。

## Core Features

- Product image upload, product analysis, and structured page planning.
- GPT-series model defaults with OpenAI-compatible Provider support.
- `gpt-image-2` first-class support for image generation and image editing.
- Visual Prompt Agent before every e-commerce and Xiaohongshu image generation.
- Batch creation for multiple product images.
- Four-step Xiaohongshu workflow: planning, prompt review, image generation, image editing.
- Generated detail page image translation through image editing.
- API usage monitor with folded retry details and final endpoint display.
- Browser-local API Key storage; API keys are not stored in the server database.
- Optional server-side locked baseURL for private deployments.

## Quick Start

```bash
npm install
npm run prisma:generate
npm run prisma:migrate
npm run dev
```

Then open the local address printed by Next.js.

## Environment

```env
DATABASE_URL="file:./dev.db"
APP_SECRET="replace-with-your-own-long-secret"
STORAGE_ROOT="./storage"
APP_RUNTIME="web"
NEXT_PUBLIC_APP_NAME="MxPage"

# Optional. When set, server-side Provider requests ignore the UI baseURL.
LOCK_BASE_URL="https://your-private-openai-compatible-gateway/v1"

# Legacy aliases are also supported.
# FORCED_API_BASE="https://your-private-openai-compatible-gateway/v1"
# FORCED_API_BASE_URL="https://your-private-openai-compatible-gateway/v1"
```

## Provider Configuration

MxPage supports OpenAI-compatible model providers. In normal mode, each browser user configures their own API Key and baseURL in the settings page. The API Key is stored only in `localStorage` and is sent to the server only for the current request.

For private deployments, set `LOCK_BASE_URL` in the server environment. When enabled, the backend always uses that baseURL regardless of what is entered in the UI, and the settings page shows the locked-channel notice.

## Default Model Policy

- Text planning and analysis prefer cost-effective GPT models such as `gpt-5-mini`, `gpt-5-nano`, `gpt-4.1-mini`, and `gpt-4o-mini`.
- Image generation and image editing prefer `gpt-image-2` when available.
- Model discovery is passive for image endpoints and does not spend image-generation quota.

## Long-Running Tasks

Long workflows use background tasks instead of one long HTTP request:

- Batch creation
- Xiaohongshu image generation
- Full detail-page language conversion
- QA-oriented workflow extensions

The frontend receives a `taskId`, polls `/api/tasks/:taskId`, and shows incremental progress. This avoids common gateway timeout issues and prevents generated images from being lost when the browser request times out.

## Scripts

```bash
npm run dev
npm run build
npm run start
npm run dist:win
npm run dist:green
```

## Desktop App

The Electron desktop build uses the same Next.js application and stores runtime data under the app data directory. Windows packaging is configured through `electron-builder`.

## Brand

Product name: MxPage

Publisher and maintainer: 灵矩绘境

Copyright (c) 2026 灵矩绘境 · MxPage

# 欢迎交流

<img width="888" height="1131" alt="_cgi-bin_mmwebwx-bin_webwxgetmsgimg__ MsgID=4406766887421910313 skey=@crypt_7a55c9cf_7083c9923764c9db3033841edabf3e22 mmweb_appid=wx_webfilehelper" src="https://github.com/user-attachments/assets/028cfd0b-a813-4655-9b49-aa9ab6619c7d" />
