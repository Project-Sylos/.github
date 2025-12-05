# **Sylos — Self-Hosted Data Migration for Power Users & Developers**

**Sylos** is a fast, private, fully self-hosted data-migration ecosystem.
Move your files anywhere — from cloud to cloud, drive to drive, NAS to PC, VM to VM, or any combo in-between! Without relying on third-party services or handing over your data.

Sylos runs entirely on **your own machines**, giving you complete control over speed, privacy, and how your migrations are executed.

This project is currently in **active early development**.
Features, APIs, and architecture are evolving rapidly as the system matures.

---

## **✨ Features**

### **⚡ Blazing-Fast Traversal & Copying**

A custom multi-round BFS traversal engine designed for extremely large directory structures. Scales from small home folders to multi-million-node migrations.

### **🔒 Completely Private**

Your data never leaves your system. There’s no cloud backend, no telemetry, no analytics, and no third-party services.

### **🧠 Smart Filtering**

Filter by:

* file type
* directory depth
* size
* regex patterns
* custom adapters

Review only what you actually want to move.

### **📝 Preview Before Executing**

Sylos shows a full preview of every change before you commit to any actual file copying or folder creation operations. Nothing happens until you approve it.

### **🛑 Pause & Resume Anytime**

Migrations survive:

* crashes
* reboots
* power loss
* application restarts

Sylos picks up exactly where you left off.

### **🔌 Modular Architecture**

Each major layer of the system is its own repo:

* **Migration Engine** → core BFS traversal + operations
* **Sylos API** → local backend + orchestration
* **Sylos UI** → native-style desktop app built for clarity
* **Sylos-FS** → filesystem adapter library
* **Spectra** → synthetic filesystem generator used for stress testing

You can use the entire ecosystem, or integrate individual layers into your own tooling.

---

## **🚀 Getting Started**

### **Downloads**

Installers and binaries are provided on the **Releases** page
*(Coming Soon — installers are still being finalized)*

### **Documentation**

Full documentation is in progress. Early guides will cover:

* How Sylos works
* Basic and advanced migrations
* Adapter development
* API workflows
* Large-scale performance tuning

Until then, the website and GitHub repos include architecture notes and examples.

### **Seperate or together?**

Sylos supports both:

* a standalone graphical desktop UI & API bundled together
* Sylos-UI.exe hostable in its own instance commmunicating with Sylos-API.exe server instance that you can run independently for advanced setups

---

## **🧱 Project Structure**

This organization contains multiple repositories:

* **`Migration-Engine`** — core traversal, actions, queueing, and crash-safe state
* **`Sylos-API`** — backend services, job orchestration, coordination, and pipeline management
* **`Sylos-UI`** — the desktop app built with modern UI tooling
* **`Spectra`** — synthetic filesystem generator for stress testing & load simulation
* **`Sylos-FS`** — shared filesystem abstraction layer for adapters/drivers
* **`project-sylos.github.io`** — the public landing page (GitHub Pages)

Each repo is self-contained but designed to interoperate cleanly.

---

## **🛠️ Roadmap (Early Development)**

Short-term goals include:

* Full cross-platform builds (Windows/Linux/macOS)
* Local-only migrations between drives, NAS, and remote mounts
* Advanced rule-based filtering
* Improved preview diff UI / UX
* Finalized job scheduling & worker orchestration
* Cleaner database abstractions across Engine/API
* Custom filesystem adapter support
* Public API documentation
* Auto-Scaler (Up and Down) for **safer & faster** performance

Long-term goals:

* Plugin-based ETL hooks
* Cloud-provider adapter support (S3, GDrive, etc.) — all self-hosted
* Migration profiles and automation recipes

---

## **📬 Community & Support**

* **Website:** [https://sylos.io](https://sylos.io)
* **GitHub:** [https://github.com/Project-Sylos](https://github.com/Project-Sylos)
* **Discord:** *[Discord](https://discord.gg/sfYCzZQNQp)*

Join the Discord if you want to follow development, ask questions, or contribute.

---

## **🤝 Contributing**

Sylos is open-source and welcomes contributions of all shapes and sizes — code, documentation, testing, UI suggestions, adapters, and performance improvements.

Contribution guidelines and style conventions will be documented soon as the architecture stabilizes.

---

## **📄 License**

Sylos components are licensed using a mix of permissive and strong-copyleft licenses depending on the repo. The main migration engine will follow a **copyleft license (LGPL)** to ensure openness while allowing commercial use.

Check each repository for its specific license.

---

## **⚠️ Alpha Notice**

Sylos is currently in early development.
Breaking changes are expected, and APIs may shift as the design evolves.

That said, the project is stable enough for experimentation, early adoption, and contributions.
