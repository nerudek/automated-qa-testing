---
name: automated-qa-testing
description: "Catch web app bugs before users do — automated exploratory QA testing"
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [qa, testing, browser, web, automated-testing, quality-assurance]
    related_skills: [dogfood]

---

# Automated QA Testing

> Catch web app bugs before users do — automated exploratory QA.

## Problem

Web applications ship with silent JavaScript errors, broken form validations, responsive layout issues, and navigation flow bugs that automated unit tests miss. Manual QA is time-consuming, inconsistent, and doesn't scale. Without a systematic approach to exploratory testing — navigating real pages, checking console logs, validating forms, and documenting evidence — bugs slip through to production.

## Overview

This repository provides a structured, agent-driven approach to automated exploratory QA testing of web applications. It combines browser automation, console log analysis, form interaction testing, and visual evidence capture into a repeatable workflow.

The core methodology is documented as a Hermes Agent skill (see [SKILL.md](./SKILL.md)) that guides you through a 5-phase process:

1. **Plan** — Scope the test, build a sitemap, identify critical paths
2. **Explore** — Navigate pages, interact with elements, check for errors
3. **Collect Evidence** — Screenshot and document each issue
4. **Categorize** — Classify by severity and type, de-duplicate
5. **Report** — Generate a structured bug report with executive summary

## Quick Start

```bash
# Clone the repository
git clone https://github.com/nerudek/automated-qa-testing.git
cd automated-qa-testing

# Read the full skill guide
cat SKILL.md
```

## How It Works

The QA workflow uses browser automation tools to:

| Step | Action |
|------|--------|
| Navigate | Load target pages via `browser_navigate` |
| Snapshot | Capture DOM structure via `browser_snapshot` |
| Inspect | Check JS console for errors via `browser_console` |
| Interact | Click buttons, fill forms, test navigation |
| Analyze | Visually assess pages via `browser_vision` |
| Verify | Test edge cases: empty states, invalid inputs, rapid clicks |

## When to Use This

- **Pre-release QA** — Before shipping a new feature or release
- **Regression testing** — After changes to existing features
- **SPA testing** — JavaScript-heavy apps with async errors
- **Form validation** — Test real-world inputs against validation logic
- **Responsive layout checks** — Identify visual breakage

## Output

For each QA session, you get:
- A structured **bug report** with severity classification
- **Screenshot evidence** for each issue
- **Console error logs** captured during testing
- **Executive summary** with issue counts and breakdowns

## Related Projects

- [dogfood](https://github.com/nerudek/dogfood) — Systematic Web Application QA Testing (Hermes Agent skill)

## License

MIT

---

**Author:** [@nerudek](https://github.com/nerudek)
If this saved you time: [PayPal.me/nerudek](https://www.paypal.me/nerudek)
