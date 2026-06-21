# AI Landing Page Generator

A full-stack web app that **automatically generates a sales landing page + Stripe Payment Link** from a simple product description — powered by the **Anthropic Claude API** with real-time streaming.

Enter a product name, description, and price. Claude writes the sales copy (hero text, features, FAQ). A live preview renders instantly. Stripe creates a payment link. Share the page via URL.

> **Live Demo**: [https://ai-landing-page-generator.vercel.app](https://ai-landing-page-generator.vercel.app) *(coming soon)*

## ✨ Features

- Product form → AI-generated sales copy in seconds
- **Real-time streaming** output (no waiting for the full response)
- Live preview of the generated landing page
- **Stripe Payment Link** auto-created with one click
- QR code generated for the payment link
- Shareable page URL (persisted via Vercel KV / Upstash)
- `.env.example` with clear setup instructions for all API keys

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 14 (App Router) |
| Language | TypeScript |
| AI / LLM | Anthropic Claude API (`claude-sonnet-4-6`) |
| Payments | Stripe API (Payment Links) |
| Styling | Tailwind CSS |
| Storage | Vercel KV (Upstash Redis) |
| Deployment | Vercel |

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- [Anthropic API key](https://console.anthropic.com/)
- [Stripe account + API key](https://stripe.com/)

### Installation

```bash
git clone https://github.com/YOSHl/ai-landing-page-generator.git
cd ai-landing-page-generator
npm install
```

Copy the example env file and fill in your keys:

```bash
cp .env.example .env.local
```

```env
ANTHROPIC_API_KEY=sk-ant-...
STRIPE_SECRET_KEY=sk_test_...
STRIPE_PUBLISHABLE_KEY=pk_test_...
KV_REST_API_URL=...
KV_REST_API_TOKEN=...
```

Run the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## 📁 Project Structure

```
ai-landing-page-generator/
├── app/
│   ├── page.tsx              # Product input form
│   ├── api/
│   │   ├── generate/         # Streaming route — Anthropic API
│   │   └── stripe/           # Stripe Payment Link creation
│   └── p/[id]/page.tsx       # Shared landing page view
├── components/
│   ├── ProductForm.tsx
│   ├── LandingPagePreview.tsx
│   └── PaymentLinkCard.tsx
├── lib/
│   ├── anthropic.ts          # Claude client
│   └── stripe.ts             # Stripe client
└── .env.example
```

## 🔑 Keywords

`Anthropic Claude API` · `Next.js` · `TypeScript` · `Stripe` · `AI` · `LLM` · `Streaming` · `Vercel` · `Full-Stack`

## 👨‍💻 Development

This project was developed with **Claude Code** (Anthropic). The entire development process — architecture design, component scaffolding, API integration, and Stripe setup — was completed using AI-assisted development. This project is itself a demonstration of the "AI-Augmented Developer" workflow.

---

## 日本語

商品説明を入力するだけで、販売ランディングページ＋Stripe決済リンクを自動生成するフルスタックWebアプリです。

### このプロジェクトについて

「AIを使っています」より「AIシステムを自分で作りました」の方が就活で何倍も強い差別化になります。このプロジェクトは、AnthropicのClaude APIを活用した実用的なAIシステムの実装例です。

### 機能

- 商品名・説明・価格を入力 → AIがセールスコピーを自動生成
- **リアルタイムストリーミング**（回答を待たずに即座に表示）
- 生成されたランディングページのライブプレビュー
- **Stripe Payment Link**の自動作成
- 決済リンクのQRコード生成
- URLによるページ共有（Vercel KV / Upstashで永続化）

### 技術構成

| レイヤー | 技術 |
|--------|------|
| フレームワーク | Next.js 14（App Router）|
| 言語 | TypeScript |
| AI / LLM | Anthropic Claude API（`claude-sonnet-4-6`）|
| 決済 | Stripe API（Payment Links）|
| スタイリング | Tailwind CSS |
| ストレージ | Vercel KV（Upstash Redis）|
| デプロイ | Vercel |

### セットアップ

```bash
git clone https://github.com/YOSHl/ai-landing-page-generator.git
cd ai-landing-page-generator
npm install
cp .env.example .env.local
# .env.local にAPIキーを設定
npm run dev
```

### 開発について

このプロジェクトは **Claude Code**（Anthropic）を活用して開発しました。アーキテクチャ設計・コンポーネントのスキャフォールド・API連携・Stripe設定のすべてにAIアシスト開発を採用しています。このプロジェクト自体が「AI活用開発者」ワークフローのデモンストレーションです。
