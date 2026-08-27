# Hi, I'm Jan Haag

Computer Science BSc student at the University of Basel, third semester, and incoming teaching assistant for the first-semester Python course. Former First Lieutenant in the Swiss Armed Forces.

What I care about is building systems and then actually running them. Most of what I write ends up deployed somewhere, with CI, monitoring, backups, and a release process attached — because the interesting problems tend to show up after the code compiles.

## Current Focus

- Backend and full-stack TypeScript: REST API design, PostgreSQL schema and migrations, authentication and sessions
- Running my own infrastructure: Docker on Linux, GitHub Actions, Prometheus and Grafana, encrypted backups with rehearsed restores
- Native macOS development in Swift 6, including signed and notarised release pipelines
- Applied machine learning and AI engineering: retrieval, embeddings, and evaluating when a model should decline to answer
- Testing as a design tool: integration, performance, and end-to-end tests that describe real behaviour

## Selected Projects

### [GymTrack](https://github.com/haagjjan/gym-track) — Full-Stack Strength Training Platform

*Project in Operation  - app.gymtrack.ch - happy to walk through the code or architecture on request.*

A workout logging and progression web app I built and operate solo, running in self-hosted production since February 2026. Roughly 38,000 lines of TypeScript, 612 commits, 18 architecture decision records.

**Tech / focus:** TypeScript, Next.js, React, Fastify, PostgreSQL, Kysely, Zod, Docker, GitHub Actions, Prometheus, Grafana, pnpm monorepo

**Highlights:** owned authentication from scratch (Argon2, database-backed opaque sessions, rate limiting, lockout, email verification); a three-job CI pipeline across 52 test files including PostgreSQL integration tests against real migrations and Playwright plus axe smoke tests; a read-count-write race on concurrent writes fixed with idempotency keys and ordered row-level locking; a curated 50-seat invite-only beta with an audit trail and GDPR-style export and erasure.

### [Tab-List](https://github.com/haagjjan/Tab-List) — Native macOS Window Switcher

A menu-bar utility for macOS 15+ on Apple Silicon that switches between individual *windows*, where the system Command-Tab collapses every window of an app into one icon. Around 18,000 lines of Swift.

**Tech / focus:** Swift 6.2, AppKit, SwiftUI, Accessibility and WindowServer APIs, XcodeGen, Sparkle, GitHub Actions

**Highlights:** cross-Space window identity through a capability-checked adapter over unsupported WindowServer APIs, with public-API fallbacks that degrade instead of crashing; a platform-free, Sendable `TabListCore` domain separated from the AppKit/SwiftUI shell, covered by 33 test targets and deterministic microbenchmarks; a two-stage release pipeline that archives, signs, notarises, staples, and verifies Gatekeeper and an EdDSA-signed Sparkle appcast, then republishes only after manual acceptance on both macOS 15 and macOS 26.

### [AI-Lab](https://github.com/haagjjan/AI-Lab) and [google-swe-rag](https://github.com/haagjjan/google-swe-rag) — RAG Pipeline and AI Engineering Sprint

A self-directed eleven-week sprint through AI engineering, with the learning logs kept in the open. Its main build is a retrieval-augmented generation system over technical PDF books, written without LangChain or a hosted vector database.

**Tech / focus:** Python, Google Gen AI SDK, NumPy, pypdf, pytest, ruff

**Highlights:** page-aware extraction, deterministic overlapping token chunking, `gemini-embedding-001` embeddings, a NumPy-persisted vector index, and cosine-similarity retrieval; answers cite document and page, and the system reports insufficient evidence rather than answering anyway; chunking, retrieval, embeddings, generation, and configuration each covered by their own test module.

### [PhantomHunt](https://github.com/haagjjan/PhantomHunt) — Asymmetric Multiplayer Java Game

A real-time 3-vs-1 multiplayer game built as a University of Basel team project: seven people, 415 commits, about 12,000 lines of Java. I contributed 103 of those commits.

**Tech / focus:** Java, JavaFX, Gradle, JUnit, JaCoCo, GitLab, TCP client-server networking

**Highlights:** engineered the server-side game state — round flow, scoring, win conditions, role-based player permissions — plus matchmaking lobbies, in-game chat, and high-score persistence. Led peer code reviews and QA planning.

### [MNIST_DNN](https://github.com/haagjjan/MNIST_DNN) — Handwritten Digit Recognition

My Matura thesis (graded 6.0 / 6.0), rebuilt in 2026 with a model registry and an interactive testing harness. A dense network reaching roughly 98% validation accuracy on MNIST, extended to hand-drawn digits through a custom preprocessing pipeline.

**Tech / focus:** Python, TensorFlow/Keras, PyTorch, NumPy, OpenCV

**What it taught me:** how much of model quality is preprocessing, and how sharply performance drops when real input stops resembling the training distribution.

## Tech Stack

**Languages:** TypeScript, Java, Python, Swift, SQL, MATLAB, Bash, HTML/CSS  
**Backend and data:** Fastify, REST APIs, PostgreSQL, Kysely, Zod, SQL migrations, authentication and sessions  
**Frontend:** Next.js, React, TanStack Query, Tailwind CSS, Recharts, SwiftUI, AppKit  
**Infrastructure and ops:** Linux, Docker and Compose, GitHub Actions, Prometheus, Alertmanager, Grafana, Restic, Cloudflare Access  
**Testing:** Playwright, JUnit, pytest, XCTest, integration, performance, and smoke tests  
**ML and AI:** PyTorch, TensorFlow, Keras, NumPy, embeddings, retrieval-augmented generation, model evaluation  
**Tools:** Git, GitHub, GitLab, Gradle, Xcode, XcodeGen, pnpm, IntelliJ IDEA, VS Code

## Contact

- GitHub: [@haagjjan](https://github.com/haagjjan)
- Email: [jan.valentin.haag@gmail.com](mailto:jan.valentin.haag@gmail.com)
- Based in Basel, Switzerland. German (native), English (fluent), French (intermediate).
