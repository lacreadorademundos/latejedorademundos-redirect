# AGENTS.md

## Project Overview

Static redirect from `latejedorademundos.com` to `www.lacreadorademundos.com`

Deployed via GitHub Pages. No build step, no dependencies

---

## Repository Structure

```
/
├── index.html    # Meta-refresh + JS redirect
├── 404.html      # Same logic for unknown routes
├── CNAME         # latejedorademundos.com
└── .gitignore
```

---

## Critical Rules

### No commit or push without explicit authorization

| Action | Allowed? |
|--------|----------|
| Read files | Yes |
| Create/modify files | Yes |
| `git status`, `git diff`, `git log` | Yes (read-only) |
| `git add` / `git commit` / `git push` | Only with explicit user authorization |

---

## Technical Notes

- `index.html` and `404.html` share the same redirect logic
- JS uses `location.replace()` to avoid back button issues
- Path, query string and hash are preserved during redirect
- `<noscript>` fallback provided with manual link
- `CNAME` must not be modified

---

## Commit Style

- **Language:** US English
- **Format:** `<type>: <description>`

| Type | Use |
|------|-----|
| `fix:` | Bug fix or HTML correction |
| `docs:` | Documentation changes |
| `chore:` | Maintenance, config |

**Examples:**
```
fix: update redirect destination URL
docs: improve README
chore: update gitignore
```
