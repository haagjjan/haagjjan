# Hi, I'm Jan

I'm a Computer Science student at the University of Basel. Most of my projects start with something I want to use myself. I enjoy building the whole thing and looking after it once people start using it.

**[haagjan.com](https://haagjan.com)** has screenshots, interactive visuals and more about me.

## Currently

- Building a platform for buying second-hand jeans with a small team at **We Want Your Jeans**.
- Giving introductory Python exercise lectures at the **University of Basel**, helping students understand the theory and apply it to programming problems.

## Projects

### GymTrack

A strength and hypertrophy training app that grew out of my own workouts. I built the web app and backend, and run it on my own servers. It has moved from a closed beta to public v0.

- **The product:** live workout logging, reusable templates and exercise-progress charts, plus weekly muscle-volume analysis with interactive 2D/3D body maps.
- **The data:** a PostgreSQL-backed API with authentication, account export and deletion. Transactions, idempotency keys and row locks protect concurrent saves; I migrated my own training history through a validated CSV import.
- **The operations:** isolated staging and production, CI with database integration and browser tests, Prometheus/Grafana monitoring and encrypted off-machine backups verified through restore tests.

TypeScript, Next.js, Fastify, PostgreSQL, Docker

[Try GymTrack](https://app.gymtrack.ch) · [Code and architecture](https://github.com/haagjjan/gym-track)

### Tab-List

A native macOS window switcher that gives each window its own entry, across applications, desktops and displays. Built around the familiar Command-Tab interaction.

- **Working with macOS:** combines Accessibility and WindowServer APIs to discover and activate windows across Spaces, with capability checks and public-API fallbacks.
- **Built to test and release:** separates the Swift domain logic from the AppKit/SwiftUI shell. CI tests on macOS 15 and 26, then handles signing, notarisation and signed Sparkle updates through separate candidate and promotion workflows.

Swift, AppKit, SwiftUI, Sparkle

[Explore Tab-List](https://github.com/haagjjan/Tab-List)

### PersSite

My personal website, built around custom 3D lettering that reacts to the pointer, scroll-driven project panels and photo collages.

Underneath, WebGL scenes share one renderer, and scrolling and animation run on the same ticker. Scenes render only while active; reduced-motion and WebGL fallbacks keep the content available across different setups.

Astro, TypeScript, Three.js, GSAP, Lenis

[Visit haagjan.com](https://haagjan.com)

### PDF retrieval and RAG

A Python project exploring when retrieved evidence helps a model answer questions about documents. I implemented the pipeline from PDF extraction and chunking to retrieval, cited answers and a FastAPI comparison interface.

- Compares dense, BM25 and hybrid retrieval, with direct-answer and oracle-context controls to help distinguish retrieval errors from generation errors.
- Includes **63 offline tests** and a **60-question evaluation set**, covering unanswerable questions and prompt-injection attempts. Live model-quality evaluation is still pending.

Python, FastAPI, NumPy

[Explore the pipeline and evaluation design](https://github.com/haagjjan/google-swe-rag)

### Handwritten digit recognition

My Matura thesis: building and evaluating a neural network for handwritten digits. It reached approximately **97.5% accuracy on the MNIST test set** and received a **6.0/6.0** thesis grade. Testing my own drawings also exposed how much input preprocessing and differences in handwriting affect the result.

Python, TensorFlow/Keras

[Code, thesis and experiments](https://github.com/haagjjan/MNIST_DNN)

## Away from code

I'm into karate and the gym. I enjoy getting out into the mountains, and I'm always up for a good coffee.

Feel free to say hello: [email](mailto:jan.valentin.haag@gmail.com) or [LinkedIn](https://www.linkedin.com/in/jan-haag-724708444/).
