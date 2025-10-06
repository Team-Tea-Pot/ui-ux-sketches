# Features Directory

This directory contains UI/UX sketches and diagrams organized by feature or user journey.

## Structure

Each feature should have its own directory with the following files:
- `<feature-name>-sketch.excalidraw` - The Excalidraw sketch file
- `<feature-name>-diagram.excalidraw` or `<feature-name>-diagram.drawio` - The flow diagram

## Example

```
features/
├── user-login/
│   ├── user-login-sketch.excalidraw
│   └── user-login-diagram.excalidraw
└── dashboard/
    ├── dashboard-sketch.excalidraw
    └── dashboard-diagram.drawio
```

## Contribution Guidelines

1. Create a feature branch from `development` for your feature/user journey
2. Create a directory for your feature under `features/`
3. Add both required files:
   - An Excalidraw sketch file
   - A diagram file (Excalidraw or Draw.io format)
4. Create a PR to merge into `development` branch
5. Both files must be present for the PR to be approved

## Naming Convention

- Use kebab-case for directory names (e.g., `user-login`, `shopping-cart`)
- Include the feature name in both file names
- Use descriptive names that clearly identify the feature
