<div align="center">

  <h1>📚 Bookified</h1>
  <p><strong>Talk to your books. Powered by AI.</strong></p>

  <div>
    <img src="https://img.shields.io/badge/-Next.js_16-000000?style=for-the-badge&logo=Next.js&logoColor=white" />
    <img src="https://img.shields.io/badge/-TypeScript-3178C6?style=for-the-badge&logo=Typescript&logoColor=white" />
    <img src="https://img.shields.io/badge/-Tailwind_CSS-06B6D4?style=for-the-badge&logo=Tailwind-CSS&logoColor=white" />
    <img src="https://img.shields.io/badge/-Shadcn/UI-000000?style=for-the-badge&logo=shadcnui&logoColor=white" /><br/>
    <img src="https://img.shields.io/badge/-Vapi-62F6B5?style=for-the-badge&logo=Vapi&logoColor=black" />
    <img src="https://img.shields.io/badge/-ElevenLabs-FFFFFF?style=for-the-badge&logo=ElevenLabs&logoColor=black" />
    <img src="https://img.shields.io/badge/-Clerk-6C47FF?style=for-the-badge&logo=Clerk&logoColor=white" />
    <img src="https://img.shields.io/badge/-MongoDB-47A248?style=for-the-badge&logo=MongoDB&logoColor=white" />
  </div>

</div>

---

## 📋 Table of Contents

1. [✨ Introduction](#introduction)
2. [⚙️ Tech Stack](#tech-stack)
3. [🔋 Features](#features)
4. [🤸 Quick Start](#quick-start)
5. [🔐 Environment Variables](#environment-variables)

---

## <a name="introduction">✨ Introduction</a>

**Bookified** is an AI-powered web application that transforms your PDF books into interactive, conversational companions. Instead of passively reading, you can upload any PDF and have a real-time, voice-driven conversation with it — asking questions, requesting summaries, or exploring ideas, all through natural speech.

The platform combines cutting-edge Voice AI (via Vapi), high-fidelity text-to-speech (via ElevenLabs), Retrieval-Augmented Generation (RAG) using Google Gemini embeddings, and a clean, modern UI — creating a unique reading experience unlike anything traditional.

Built with **Next.js 16**, **TypeScript**, **MongoDB**, **Clerk**, and **Tailwind CSS / Shadcn UI**, Bookified is a full-stack, production-ready application with secure authentication, cloud file storage, and scalable database architecture.

---

## <a name="tech-stack">⚙️ Tech Stack</a>

| Technology | Role |
|---|---|
| **[Next.js 16](https://nextjs.org/docs)** | Full-stack React framework for UI, server-side rendering, and API routes |
| **[TypeScript](https://www.typescriptlang.org/)** | Type-safe development across the entire codebase |
| **[Tailwind CSS v4](https://tailwindcss.com/)** | Utility-first CSS framework for rapid, responsive styling |
| **[Shadcn UI](https://ui.shadcn.com/)** | Accessible, composable component library built on Radix UI |
| **[Clerk](https://clerk.com/)** | Authentication and user management (email + social login) |
| **[Vapi](https://vapi.ai/)** | Real-time Voice AI platform for low-latency voice conversations |
| **[ElevenLabs](https://elevenlabs.io/)** | Lifelike AI voice synthesis for audio persona previews |
| **[Google Gemini](https://aistudio.google.com/)** | AI embeddings for semantic text understanding and RAG |
| **[MongoDB + Mongoose](https://www.mongodb.com/)** | NoSQL database for storing books, users, and transcripts |
| **[Vercel Blob](https://vercel.com/docs/storage/vercel-blob)** | Cloud storage for uploaded PDF files |
| **[pdf.js (pdfjs-dist)](https://mozilla.github.io/pdf.js/)** | Client-side PDF text extraction |
| **[React Hook Form + Zod](https://react-hook-form.com/)** | Form state management and schema validation |

---

## <a name="features">🔋 Features</a>

- **📄 PDF Upload & Ingestion** — Upload any PDF book; the app automatically extracts text, chunks it, and generates vector embeddings for semantic retrieval.

- **🎙️ Voice Conversations** — Engage in real-time, back-and-forth voice dialogues with your uploaded books using natural speech, powered by Vapi.

- **🤖 AI Voice Personas** — Browse and preview a variety of AI voice personas powered by ElevenLabs to find your perfect reading companion.

- **🔍 Retrieval-Augmented Generation (RAG)** — Questions are answered using relevant context retrieved from the book's actual content via semantic vector search.

- **📝 Session Transcripts** — Automatic text transcripts are generated for every voice conversation so you never lose a key insight.

- **📚 Library Management** — Browse your personal uploads and a shared global library, with search functionality to quickly find books.

- **🔐 Secure Authentication** — User sign-up, sign-in, and session management handled via Clerk with support for email and social providers.

- **☁️ Cloud File Storage** — PDFs are stored securely in Vercel Blob storage and linked to each user's profile.

- **🌙 Dark Mode** — Full dark/light theme support via `next-themes`.

---

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up and run Bookified locally.

### Prerequisites

Make sure you have the following installed:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en) (v18 or later recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### 1. Clone the Repository

```bash
git clone https://github.com/Nmigdadi/Bookified.git
cd bookified
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root of the project and add the following variables (see the [Environment Variables](#environment-variables) section for details):

```env
NODE_ENV='development'
NEXT_PUBLIC_BASE_URL=http://localhost:3000

# CLERK
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_SIGN_IN_FALLBACK_REDIRECT_URL=/
NEXT_PUBLIC_CLERK_SIGN_UP_FALLBACK_REDIRECT_URL=/

# VERCEL BLOB
BLOB_READ_WRITE_TOKEN=

# MONGODB
MONGODB_URI=

# VAPI
NEXT_PUBLIC_ASSISTANT_ID=
NEXT_PUBLIC_VAPI_API_KEY=
VAPI_SERVER_SECRET=

# GOOGLE GEMINI (for embeddings)
GOOGLE_GEMINI_API_KEY=

# ELEVENLABS
ELEVENLABS_API_KEY=
```

### 4. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the app.

---

## <a name="environment-variables">🔐 Environment Variables</a>

You'll need accounts and API keys from the following services:

| Variable | Description | Where to Get It |
|---|---|---|
| `NEXT_PUBLIC_BASE_URL` | The base URL of your app (e.g. `http://localhost:3000`) | Self-defined |
| `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` | Clerk public key | [clerk.com](https://clerk.com) → Dashboard → API Keys |
| `CLERK_SECRET_KEY` | Clerk secret key | [clerk.com](https://clerk.com) → Dashboard → API Keys |
| `BLOB_READ_WRITE_TOKEN` | Vercel Blob storage token | [vercel.com](https://vercel.com) → Storage → Blob |
| `MONGODB_URI` | MongoDB connection string | [mongodb.com](https://www.mongodb.com) → Atlas → Connect |
| `NEXT_PUBLIC_ASSISTANT_ID` | Your Vapi assistant ID | [vapi.ai](https://vapi.ai) → Assistants |
| `NEXT_PUBLIC_VAPI_API_KEY` | Vapi public API key | [vapi.ai](https://vapi.ai) → Account → API Keys |
| `VAPI_SERVER_SECRET` | Vapi server-side secret for webhook validation | [vapi.ai](https://vapi.ai) → Account → API Keys |
| `GOOGLE_GEMINI_API_KEY` | Google Gemini API key for generating embeddings | [aistudio.google.com](https://aistudio.google.com) → Get API Key |
| `ELEVENLABS_API_KEY` | ElevenLabs API key for voice synthesis | [elevenlabs.io](https://elevenlabs.io) → Profile → API Key |

> **Note:** Never commit your `.env` file to version control. It is already listed in `.gitignore`.

---

## 📁 Project Structure

```
bookified/
├── app/                  # Next.js App Router (pages, layouts, API routes)
│   ├── (root)/           # Main application pages
│   ├── api/              # Server-side API routes (upload, Vapi webhooks, etc.)
│   └── books/            # Book detail and conversation pages
├── components/           # Reusable React components
├── database/             # Mongoose models and database connection
├── hooks/                # Custom React hooks
├── lib/                  # Utility functions (Vapi, ElevenLabs, embeddings, etc.)
├── public/               # Static assets
├── types.d.ts            # Global TypeScript type definitions
└── .env                  # Environment variables (not committed)
```

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).
