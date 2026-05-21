# TrustyAI Organization Templates

Shared GitHub Actions workflows and configurations for TrustyAI repositories.

## Available Workflow Templates

### Unicode Safety Check

Detects hidden unicode characters used in ASCII smuggling attacks.

**When to use:** Any repo with:
- Markdown documentation
- AI context files (CLAUDE.md, AGENTS.md, skills)
- Code accepting external contributions

**Attack vectors detected:**
- Tag characters (U+E0001-E007F) - primary smuggling vector
- Zero-width characters (invisible joiners/spaces)
- Bidi overrides (Trojan Source CVE-2021-42574)
- Homoglyphs (Cyrillic/Greek lookalikes)
- Variation selectors (Glassworm encoding)
- Private Use Area characters
- 14 additional detection rules

**How to add:**
1. Go to your repo → Actions → New workflow
2. Find "Unicode Safety Check" in suggested workflows
3. Click "Configure"
4. Commit to default branch

**Features:**
- Runs on pull requests (scans changed files only)
- Weekly full repo scan (Sundays 3 AM UTC)
- Manual trigger via workflow_dispatch
- Minimal configuration required (customize branches if needed)

**Optional: Pre-commit hook integration**

For local development protection, add to `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/dcondrey/unicode-safety-check
    rev: v3.0.0
    hooks:
      - id: unicode-safety-check
        name: Check for hidden unicode characters
```

See [template source](workflow-templates/unicode-safety.yml) for implementation details.

**Note:** Template triggers on `main`, `master`, and `develop` branches. Customize `branches:` list for your repo's branch strategy.

## References

- [ASCII Smuggling: A Threat Hidden in Plain Sight](https://marcogerber.ch/ascii-smuggling-a-threat-hidden-in-plain-sight/)
- [Microsoft CVE-2025-32711 (EchoLeak)](https://www.cve.org/CVERecord?id=CVE-2025-32711)
- [Trojan Source CVE-2021-42574](https://www.cve.org/CVERecord?id=CVE-2021-42574)
- [dcondrey/unicode-safety-check](https://github.com/dcondrey/unicode-safety-check)
