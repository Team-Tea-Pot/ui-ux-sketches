# Workflow Process

This document outlines the complete workflow for contributing UI/UX sketches to this repository.

## 📊 Contribution Flow

```
┌─────────────────────────────────────────────────────────────┐
│                    Start Contribution                        │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  1. Create Feature Branch from 'development'                 │
│     git checkout development                                 │
│     git checkout -b feature/your-feature-name                │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  2. Create Feature Directory                                 │
│     mkdir -p features/your-feature-name                      │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  3. Create Sketch in Excalidraw                              │
│     → Go to https://excalidraw.com/                          │
│     → Create your UI sketch                                  │
│     → Save as: your-feature-name-sketch.excalidraw           │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  4. Create Diagram                                           │
│     Option A: Excalidraw (https://excalidraw.com/)           │
│     → Save as: your-feature-name-diagram.excalidraw          │
│                                                              │
│     Option B: Draw.io (https://app.diagrams.net/)            │
│     → Save as: your-feature-name-diagram.drawio              │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  5. Commit and Push                                          │
│     git add features/your-feature-name/                      │
│     git commit -m "Add [feature] sketch and diagram"         │
│     git push origin feature/your-feature-name                │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  6. Create Pull Request to 'development' branch              │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│  7. Automated Validation (GitHub Actions)                    │
│     ✓ Check for sketch file (-sketch.excalidraw)             │
│     ✓ Check for diagram file (-diagram.excalidraw/.drawio)   │
└─────────────────────┬───────────────────────────────────────┘
                      │
              ┌───────┴────────┐
              │                │
              ▼                ▼
         ┌─────────┐      ┌─────────┐
         │  PASS   │      │  FAIL   │
         └────┬────┘      └────┬────┘
              │                │
              ▼                ▼
    ┌──────────────────┐  ┌──────────────────┐
    │ Team Review      │  │ Fix Missing      │
    │                  │  │ Files & Push     │
    └────┬─────────────┘  └────┬─────────────┘
         │                     │
         │                     │
         └──────────┬──────────┘
                    │
                    ▼
         ┌────────────────────┐
         │ Merge to           │
         │ 'development'      │
         └────────┬───────────┘
                  │
                  ▼
         ┌────────────────────┐
         │ Eventually         │
         │ Merge to 'master'  │
         └────────────────────┘
```

## 🔄 Branch Strategy

```
master (production)
  │
  ├── development (active development)
  │     │
  │     ├── feature/user-login
  │     │     └── PR → development
  │     │
  │     ├── feature/dashboard
  │     │     └── PR → development
  │     │
  │     └── feature/shopping-cart
  │           └── PR → development
  │
  └── (periodic merges from development)
```

## ✅ Validation Rules

The GitHub Actions workflow validates:

| Check | Requirement | Example |
|-------|-------------|---------|
| Sketch File | Must end with `-sketch.excalidraw` | `user-login-sketch.excalidraw` ✓ |
| Diagram File | Must end with `-diagram.excalidraw` or `-diagram.drawio` | `user-login-diagram.drawio` ✓ |
| Location | Must be in `features/` directory | `features/user-login/` ✓ |
| Count | At least 1 of each type | 1 sketch + 1 diagram = ✓ |

## 🚫 Common Issues

### Issue: "No sketch or diagram files found"
- **Cause:** Files are not in the `features/` directory
- **Fix:** Move files to `features/your-feature-name/`

### Issue: "PR must include BOTH files"
- **Cause:** Missing either sketch or diagram file
- **Fix:** Add the missing file with correct naming

### Issue: Validation passes but files have wrong names
- **Cause:** Files don't follow naming convention
- **Note:** Validation checks for `-sketch.excalidraw` and `-diagram.excalidraw/.drawio` suffixes

## 📞 Getting Help

1. Check [README.md](README.md) for overview
2. Check [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guide
3. Check [QUICK_START.md](QUICK_START.md) for quick reference
4. Open an issue if you need help
