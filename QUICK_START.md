# Quick Reference Guide

## ⚡ Quick Start

### For Contributors

1. **Create a feature branch from `development`:**
   ```bash
   git checkout development
   git checkout -b feature/your-feature-name
   ```

2. **Create your feature directory:**
   ```bash
   mkdir -p features/your-feature-name
   ```

3. **Add both required files:**
   - `your-feature-name-sketch.excalidraw` (from Excalidraw)
   - `your-feature-name-diagram.excalidraw` or `.drawio` (from Excalidraw or Draw.io)

4. **Submit PR to `development` branch**

---

## 📋 File Requirements

### ✅ Valid PR Example

```
features/user-login/
├── user-login-sketch.excalidraw    ✓ Required
└── user-login-diagram.excalidraw   ✓ Required
```

### ❌ Invalid PR Examples

**Missing diagram:**
```
features/user-login/
└── user-login-sketch.excalidraw    ✓
```

**Wrong naming:**
```
features/user-login/
├── sketch.excalidraw               ✗ (missing feature name)
└── diagram.drawio                  ✗ (missing feature name)
```

**Wrong file type for sketch:**
```
features/user-login/
├── user-login-sketch.drawio        ✗ (must be .excalidraw)
└── user-login-diagram.excalidraw   ✓
```

---

## 🎨 Tools

- **Excalidraw:** https://excalidraw.com/
- **Draw.io:** https://app.diagrams.net/

---

## 📝 Naming Rules

- **Directory:** `kebab-case` (e.g., `user-login`, `shopping-cart`)
- **Sketch:** `<feature>-sketch.excalidraw`
- **Diagram:** `<feature>-diagram.excalidraw` or `<feature>-diagram.drawio`

---

## 🔍 What Gets Validated?

The GitHub Actions workflow checks:

1. ✅ At least one file ending with `-sketch.excalidraw`
2. ✅ At least one file ending with `-diagram.excalidraw` or `-diagram.drawio`
3. ✅ Files are in the `features/` directory

---

## 📚 More Information

- **Full Guide:** See [README.md](README.md)
- **Detailed Instructions:** See [CONTRIBUTING.md](CONTRIBUTING.md)
- **Features Directory:** See [features/README.md](features/README.md)
- **Example:** See [features/.example-feature/](features/.example-feature/)
