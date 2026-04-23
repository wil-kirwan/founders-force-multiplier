# HighLevel skill pack repo

This repo packages the shared HighLevel handler skill together with a migration kit for your existing skill library.

## Included

- `skills/highlevel-api/`
  - `SKILL.md`
  - `highlevel_universal_handler.py`
  - `highlevel_universal_handler/` package with examples, seed registry, tests, and docs
- `skills/` — concrete updated `SKILL.md` files for uploaded skills
- `migration/skills-highlevel-manifest.csv`
- `migration/skills-highlevel-manifest.json`
- `migration/overlays/`
- `migration/generated-updated-skills/`
- `scripts/install_highlevel_skill_pack.py`
- `docs/UPDATED_SKILLS.md`

## Review summary

- Total skills reviewed from the supplied matrix: 59
- Required updates: 9
- Optional updates: 32
- No update needed: 18

## Concrete skills currently included as full files

### Existing concrete skills
- `seo-programmatic`
- `seo-sitemap`
- `shopify-store-design`
- `topic-researcher`
- `transcript`

### Batch 1 concrete skills
- `ads`
- `ads-audit`
- `ads-google`
- `ads-landing`
- `ads-linkedin`
- `ads-meta`
- `ads-microsoft`
- `ads-plan`
- `ads-tiktok`
- `ads-youtube`
- `blog`
- `blog-analyze`
- `blog-audit`
- `blog-brief`
- `blog-calendar`
- `blog-geo`
- `blog-repurpose`
- `blog-rewrite`
- `blog-schema`
- `blog-seo-check`
- `blog-strategy`
- `blog-write`
- `carousel-gen`
- `client-brief`
- `content-master`
- `content-scripting`
- `ecommerce-cro`
- `gdocs-setup`
- `hand-raiser`
- `hooks`
- `notion-setup`
- `seo`
- `seo-audit`
- `seo-competitor-pages`
- `seo-geo`
- `seo-page`
- `seo-plan`
- `seo-schema`
- `seo-technical`

## Quick install into an existing skill library

```bash
python scripts/install_highlevel_skill_pack.py --skills-root ~/.claude/skills
```

Dry run:

```bash
python scripts/install_highlevel_skill_pack.py --skills-root ~/.claude/skills --dry-run
```

## What the installer does

1. Copies `skills/highlevel-api/` into the target skill root.
2. Applies merge-ready overlay blocks to any skill in the target root that matches the manifest and has a `SKILL.md`.
3. Leaves `No` skills untouched.
4. Creates `.bak` backups before modifying an existing skill file.

## Notes

- The repo now includes full updated versions of the first two uploaded batches.
- Overlay files remain available for merge-based installs and for skills that have not yet been provided as full source files.
- The repo is git-initialized so each batch can be committed cleanly.
