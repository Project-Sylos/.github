# Sylos - Self-Hosted File Migration for Everyone

Sylos is a fast, private, fully self-hosted data migration ecosystem.
Move your files anywhere: from cloud to cloud, drive to drive, NAS to PC, VM to VM, or any combination in between. No third-party services. No remote servers. No loss of control.

Everything runs on your own machines.
You decide how fast, how safe, and how private your migrations are.

Sylos is in active early development. Features and architecture may evolve as the project grows.

---

## Features

### Fast Traversal and Copying

A custom multi-round BFS traversal engine built for extremely large directory structures. Handles everything from small home folders to multi-million-node migrations.

### Complete Privacy

Your data always stays on your system.
No cloud backends. No telemetry. No analytics. No external processing.

### Smart Filtering

Filter by file type, directory depth, size, regex patterns, or write your own adapter rules.
Move exactly what you want and nothing more.

### Preview Before Executing

Sylos shows a complete preview of all planned operations before anything is copied or created. Review changes with confidence and avoid accidental overwrites.

### Pause and Resume Anytime

Migrations survive crashes, reboots, power loss, and application restarts.
Sylos always picks up exactly where you left off.

### Modular Architecture

Each major layer of Sylos lives in its own repository:

* Migration Engine: core traversal, actions, queueing, crash-safe state
* Sylos API: backend orchestration and job management
* Sylos UI: desktop interface
* Sylos-FS: filesystem adapter and driver layer
* Spectra: synthetic filesystem generator for testing and simulation

You can run the whole ecosystem or use only the components you need.

---

## Getting Started

### Downloads

Installers and binaries will be available on the Releases page.
(Coming soon. Packaging is in progress.)

### Documentation

Full documentation is being written as the architecture stabilizes. Planned topics include:

* how Sylos works
* example migrations
* advanced filtering
* adapter development
* API workflows
* performance tuning

Until then, the website and repositories contain architectural notes and examples.

### Run Together or Separately

Sylos supports both:

* a standalone desktop app (UI and API bundled together)
* a separate UI and API setup where the UI connects to a dedicated API server

---

## Project Structure

This organization contains several repositories:

* Migration-Engine
* Sylos-API
* Sylos-UI
* Spectra
* Sylos-FS
* project-sylos.github.io (public website)

Each repo is independent but designed to integrate cleanly with the others.

---

## Roadmap (Early Development)

Short-term goals:

* Cross-platform support (Windows, Linux, macOS)
* Local migrations across drives, NAS devices, and network mounts
* Advanced rule-based filtering
* Improved preview UI and diff clarity
* Finalized job scheduling and worker orchestration
* Cleaner database abstractions
* Public API documentation
* Auto-scaling of workers for safer and faster performance

Long-term goals:

* Plugin-based ETL hooks
* Cloud-provider adapters (S3, Google Drive, etc.), all self-hosted
* Migration profiles and reusable automation recipes

---

## Community and Support

* Website: [https://sylos.io](https://sylos.io)
* GitHub: [https://github.com/Project-Sylos](https://github.com/Project-Sylos)
* Discord: [https://discord.gg/sfYCzZQNQp](https://discord.gg/sfYCzZQNQp)

Join the community to follow development and participate in discussions.

---

## Contributing

Sylos welcomes contributions of all kinds: code improvements, documentation, adapters, UI suggestions, performance ideas, bug reports, and testing.

Contribution guidelines will be added once the architecture is more stable.

---

## License

Sylos uses different licenses depending on the repository.
The main migration engine uses LGPL to ensure openness while still allowing commercial use.

Check each repo for its specific license.

---

## Alpha Notice

Sylos is still early in development.
Breaking changes may occur while systems and APIs mature.

The project is stable enough for experimentation and early adoption.

