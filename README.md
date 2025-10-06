# ui-ux-sketches

All the sketch level developments of the teapot

## 📋 Overview

This repository contains UI/UX sketches and flow diagrams for the Team Tea Pot project. All design work is organized by feature or user journey to ensure easy navigation and contribution.

## 🌳 Branch Structure

- **`master`** - Main branch (production-ready designs)
- **`development`** - Active development branch (all PRs should target this branch)
- **`feature/*`** - Feature branches for individual features or user journeys

## 📁 Repository Structure

```
ui-ux-sketches/
├── features/
│   ├── feature-name-1/
│   │   ├── feature-name-1-sketch.excalidraw
│   │   └── feature-name-1-diagram.excalidraw
│   ├── feature-name-2/
│   │   ├── feature-name-2-sketch.excalidraw
│   │   └── feature-name-2-diagram.drawio
│   └── README.md
├── .github/
│   ├── workflows/
│   │   └── validate-pr-files.yml
│   └── PULL_REQUEST_TEMPLATE.md
└── README.md
```

## 🚀 Contribution Workflow

### 1. Create a Feature Branch

```bash
git checkout development
git pull origin development
git checkout -b feature/your-feature-name
```

### 2. Create Your Feature Directory

```bash
mkdir -p features/your-feature-name
```

### 3. Add Required Files

Every feature **must** include both files:

- **Sketch file**: `your-feature-name-sketch.excalidraw`
- **Diagram file**: `your-feature-name-diagram.excalidraw` or `your-feature-name-diagram.drawio`

Example:
```bash
features/user-login/
├── user-login-sketch.excalidraw
└── user-login-diagram.excalidraw
```

### 4. Create a Pull Request

1. Commit your changes
2. Push to your feature branch
3. Open a PR targeting the `development` branch
4. Fill out the PR template with required information

### 5. PR Requirements

✅ **Your PR will be automatically validated and must include:**

1. At least one Excalidraw sketch file ending with `-sketch.excalidraw`
2. At least one diagram file ending with `-diagram.excalidraw` or `-diagram.drawio`

❌ **PRs will fail validation if:**

- No sketch file is included
- No diagram file is included
- Files are not in the `features/` directory
- Files don't follow the naming convention

## 📝 Naming Conventions

- **Directory names**: Use kebab-case (e.g., `user-login`, `shopping-cart`, `checkout-flow`)
- **File names**: Include the feature name and type:
  - Sketch: `<feature-name>-sketch.excalidraw`
  - Diagram: `<feature-name>-diagram.excalidraw` or `<feature-name>-diagram.drawio`

## 🛠️ Tools

- **Excalidraw**: https://excalidraw.com/ - For sketches and diagrams
- **Draw.io**: https://app.diagrams.net/ - Alternative for flow diagrams

## ❓ FAQ

**Q: Can I use Draw.io for both the sketch and diagram?**
A: The sketch must be an Excalidraw file (`.excalidraw`). The diagram can be either Excalidraw (`.excalidraw`) or Draw.io (`.drawio`).

**Q: Can I include multiple features in one PR?**
A: Yes, as long as each feature has both required files (sketch and diagram).

**Q: What if I need to update an existing feature?**
A: Create a feature branch, make your changes, and submit a PR as usual. The validation will pass as long as both files are present.

**Q: Can I add additional files (e.g., mockups, images)?**
A: Yes, you can add supplementary files to your feature directory, but the two required files must always be present.

## 📧 Support

If you have questions or need help, please open an issue or contact the team.
