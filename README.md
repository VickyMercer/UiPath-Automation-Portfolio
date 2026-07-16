# UiPath Automation Portfolio

A hands-on collection of UiPath RPA projects built while learning and practicing Robotic Process Automation — spanning core programming fundamentals, web and desktop UI automation, Excel and PDF data processing, and modular workflow design.

## About This Repository

Every project here was built, tested, and documented individually in UiPath Studio. The repository is organized to reflect a genuine learning progression — starting with core programming logic (loops, arrays, dictionaries, string parsing) and building up to full RPA workflows involving browser automation, desktop applications, Excel/PDF data handling, and multi-file modular automation design.

`Fundamentals/` contains early exercises in core programming logic; the main portfolio folder contains RPA-focused automations, in progression from basic to intermediate to advanced. This framing turns the simple projects into a feature — they show the groundwork the more advanced automations are built on, not just a pile of practice files.

## Repository Contents

**RPA-Focused Automations** (repository root)
Projects that interact with real applications and interfaces — practiced against UiPath's official training tools (the ACME test website and the DoubleUI desktop app):
- Web automation: login flows, form entry, multi-step registration, paginated data extraction
- Desktop application automation (non-browser UI interaction)
- Excel-based automations: reading, filtering, calculating, and writing data back to workbooks
- PDF text extraction and file generation
- Modular, multi-file workflows using invoked workflows and shared session/browser state across files

**Fundamentals** (`Fundamentals/` subfolder)
Pure programming-logic exercises with no UI or application interaction — the building blocks:
- Arrays, lists, and dictionaries (building, sorting, filtering, counting)
- Conditional logic and switch-based branching
- String parsing and text manipulation
- Loops, recursion-style calculations, and invoked-workflow argument passing (In/Out/InOut)

## Skills Demonstrated

- UI automation (web and desktop) using Selector and Computer Vision-based targeting, with fallback/self-healing strategies
- Modular automation design — breaking logic into reusable invoked workflow files with clean argument passing
- Data manipulation with DataTables, Excel workbooks, and PDF documents
- Core programming constructs: loops, conditionals, collections, string operations
- Structured, professional documentation — every project folder includes its own README covering overview, logic, workflow, output, and requirements

## Repository Structure

```
UiPath-Automation-Portfolio/
├── Fundamentals/          # Pure programming-logic projects
│   ├── ProjectName/
│   │   ├── Main.xaml
│   │   └── README.md
│   └── ...
├── ProjectName/           # RPA-focused automations (repo root)
│   ├── Main.xaml
│   └── README.md
├── ...
└── README.md              # You are here
```

Each project folder is self-contained and includes its own `README.md` with a full breakdown — overview, step-by-step logic, workflow files, output, key concepts practiced, and requirements. Browse the folders above to explore individual projects.

## Tools & Technologies

- UiPath Studio
- UiPath Excel, PDF, and UI Automation activity packages
- Git & GitHub for version control

## License

This repository is licensed under the [MIT License](LICENSE) — feel free to explore, learn from, or reference these projects.
