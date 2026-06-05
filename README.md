# ⚡ Eigen

**AI-first cloud IDE built for modern developers.**

> Write code, collaborate in real time, interact with AI agents, manage projects, and accelerate development workflows from a single intelligent workspace.

---

## ✨ Features

**🤖 AI-Powered Development**
Experience context-aware AI code assistance, intelligent code suggestions, and natural language code generation. Features include Quick Edit (`Cmd + K`), an AI conversation sidebar, and built-in debugging assistance.

**💻 Modern Code Editor**
A VS Code-inspired editing experience featuring multi-language syntax highlighting, code folding, minimap, multi-cursor editing, bracket matching, indentation guides, and seamless tab-based navigation.

**📁 Project Management**
Robust multi-file project support with a visual file explorer. Manage folder hierarchies, create/rename/move/delete files, and rely on secure auto-save functionality—all managed from a central project dashboard.

**🤝 Real-Time Collaboration**
Built for teams with instant synchronization, optimistic UI updates, real-time database integration, and reliable background task processing.

**⚡ Developer Experience (DX)**
Secure authentication via Clerk (with GitHub support), a fully responsive interface, native dark mode, resizable panels, and a modern, scalable architecture.

---

## 🛠 Tech Stack

| Category | Technologies |
| --- | --- |
| **Frontend** | Next.js 16, React 19, TypeScript, Tailwind CSS 4 |
| **Editor Core** | CodeMirror 6 |
| **Backend** | Convex, Inngest |
| **AI Integration** | Claude Sonnet, Gemini |
| **Authentication** | Clerk |
| **Execution** | WebContainer API, xterm.js |
| **UI Components** | shadcn/ui, Radix UI |

---

## 🚀 Getting Started

### Prerequisites

* **Node.js:** v20 or higher
* **Package Manager:** npm or pnpm
* **Required Services:** Clerk, Convex, Inngest, Anthropic API (or Google AI Studio)

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/eigen.git
cd eigen

```

### 2. Install dependencies

```bash
npm install

```

### 3. Configure environment variables

```bash
cp .env.example .env.local

```

Update your `.env.local` with the following credentials:

```env
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_publishable_key
CLERK_SECRET_KEY=your_secret_key

# Convex Real-time Database
NEXT_PUBLIC_CONVEX_URL=your_convex_url
CONVEX_DEPLOYMENT=your_convex_deployment
EIGEN_CONVEX_INTERNAL_KEY=your_internal_key

# AI Providers
ANTHROPIC_API_KEY=your_anthropic_key
GOOGLE_GENERATIVE_AI_API_KEY=your_gemini_key

# Optional Configurations
FIRECRAWL_API_KEY=your_firecrawl_key
SENTRY_DSN=your_sentry_dsn

```

### 4. Start the development services

You will need to run these commands in separate terminal windows to spin up the full local environment:

**Terminal 1: Start Convex**

```bash
npx convex dev

```

**Terminal 2: Start Next.js Client**

```bash
npm run dev

```

**Terminal 3: Start Inngest (Background Jobs)**

```bash
npx inngest-cli@latest dev

```

Once all services are running, open **`http://localhost:3000`** in your browser.

---

## 📂 Project Structure

```text
eigen/
├── src/
│   ├── app/                 # Next.js App Router
│   ├── components/          # Reusable UI components
│   ├── features/            # Feature-based module grouping
│   ├── inngest/             # Background job configurations
│   └── lib/                 # Utility functions and shared logic
└── convex/                  # Real-time backend
    ├── schema.ts            # Database schema definitions
    ├── projects.ts          # Project management logic
    ├── files.ts             # File system operations
    ├── conversations.ts     # AI chat history and state
    └── system.ts            # Core system events

```

---

## ⚙️ Core Functionality

| Module | Capabilities |
| --- | --- |
| **Language Support** | JavaScript, TypeScript, HTML, CSS, JSON, Markdown, Python |
| **AI Workspace** | Conversations, quick edits, code suggestions, context-aware help |
| **File System** | Hierarchical folders, file management, auto-save, fast navigation |
| **Infrastructure** | Live live updates, background jobs, event-driven workflows |

---

## 📜 Available Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Starts the local development server |
| `npm run build` | Builds the application for production |
| `npm run start` | Starts the production server |
| `npm run lint` | Runs ESLint to check for code issues |

---

## 🗺 Roadmap

* [ ] Integration of Advanced AI agents
* [ ] Native GitHub repository integration
* [ ] AI-driven project scaffolding and generation
* [ ] Enhanced multiplayer collaboration features
* [ ] WebContainer application previews
* [ ] Integrated terminal improvements
* [ ] Deep workspace and layout customization

---

## 💡 Inspiration

Eigen is inspired by the next generation of AI-native developer tools and modern cloud-based development environments. It aims to bridge the gap between intelligent AI assistance and a powerful, latency-free coding experience.

## 📄 License

This project is licensed under the **MIT License**.






