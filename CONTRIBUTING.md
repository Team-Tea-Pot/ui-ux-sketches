# Contributing to UI/UX Sketches

Thank you for contributing to the Team Tea Pot UI/UX sketches repository! This guide will help you get started.

## Getting Started

1. **Fork the repository** (if you don't have write access)
2. **Clone your fork** or the main repository
3. **Create a feature branch** from `development`

```bash
git checkout development
git pull origin development
git checkout -b feature/your-feature-name
```

## Creating Your Feature

### Step 1: Create Feature Directory

Create a directory for your feature under `features/`:

```bash
mkdir -p features/your-feature-name
```

Use kebab-case for directory names (e.g., `user-login`, `shopping-cart`).

### Step 2: Create Required Files

Every feature submission **must** include two files:

1. **Sketch file** (Excalidraw format)
   - Name: `your-feature-name-sketch.excalidraw`
   - Create at: https://excalidraw.com/
   - Purpose: Initial UI sketches and wireframes

2. **Diagram file** (Excalidraw or Draw.io format)
   - Name: `your-feature-name-diagram.excalidraw` or `your-feature-name-diagram.drawio`
   - Create at: https://excalidraw.com/ or https://app.diagrams.net/
   - Purpose: Flow diagrams, user journeys, or process flows

### Example Structure

```
features/user-login/
├── user-login-sketch.excalidraw      # Required: UI sketches
└── user-login-diagram.excalidraw     # Required: Flow diagram
```

## File Naming Convention

- **Directories**: `kebab-case` (lowercase, hyphens between words)
  - ✅ `user-login`
  - ✅ `shopping-cart`
  - ❌ `UserLogin`
  - ❌ `shopping_cart`

- **Sketch files**: `<feature-name>-sketch.excalidraw`
  - ✅ `user-login-sketch.excalidraw`
  - ❌ `user-login.excalidraw`
  - ❌ `sketch.excalidraw`

- **Diagram files**: `<feature-name>-diagram.[excalidraw|drawio]`
  - ✅ `user-login-diagram.excalidraw`
  - ✅ `user-login-diagram.drawio`
  - ❌ `user-login-flow.excalidraw`
  - ❌ `diagram.drawio`

## Creating Sketches and Diagrams

### Using Excalidraw

1. Go to https://excalidraw.com/
2. Create your sketch or diagram
3. Click the menu (☰) → "Save as..."
4. Save the `.excalidraw` file to your feature directory

### Using Draw.io

1. Go to https://app.diagrams.net/
2. Create your diagram
3. File → Save As → Device
4. Save as `.drawio` format to your feature directory

## Submitting Your Work

### Step 1: Commit Your Changes

```bash
git add features/your-feature-name/
git commit -m "Add [feature-name] sketch and diagram"
```

### Step 2: Push to Your Branch

```bash
git push origin feature/your-feature-name
```

### Step 3: Create a Pull Request

1. Go to the repository on GitHub
2. Click "New Pull Request"
3. **Base branch**: `development`
4. **Compare branch**: `feature/your-feature-name`
5. Fill out the PR template

### Step 4: Wait for Validation

Your PR will be automatically validated by GitHub Actions. The validation checks:

✅ At least one sketch file with `-sketch.excalidraw` suffix
✅ At least one diagram file with `-diagram.excalidraw` or `-diagram.drawio` suffix

If validation fails, add the missing file(s) and push again.

## PR Review Process

1. **Automated validation** runs on your PR
2. **Team review** of your sketches and diagrams
3. **Feedback** may be provided for revisions
4. **Merge** to `development` once approved

## Best Practices

### Organization

- Keep related sketches in the same feature directory
- Use descriptive feature names
- One feature per directory

### Quality

- Ensure sketches are clear and readable
- Include labels and annotations where helpful
- Flow diagrams should clearly show user journeys or processes

### Collaboration

- Review existing features before creating similar ones
- Consider combining related features
- Ask questions in issues or discussions

## Common Issues

### Issue: PR validation fails with "No sketch or diagram files found"

**Solution**: Ensure your files are in the `features/` directory and follow the naming convention.

### Issue: Validation says "Must include BOTH a sketch file and a diagram file"

**Solution**: You're missing one of the required files. Add:
- A file ending with `-sketch.excalidraw`, OR
- A file ending with `-diagram.excalidraw` or `-diagram.drawio`

### Issue: File format not recognized

**Solution**: Ensure you're using the correct file extensions:
- `.excalidraw` for Excalidraw files
- `.drawio` for Draw.io files

## Questions?

If you have questions or run into issues:

1. Check the [README.md](README.md) for general information
2. Review the [features/README.md](features/README.md) for structure details
3. Open an issue for help
4. Contact the team

Thank you for contributing! 🎨
