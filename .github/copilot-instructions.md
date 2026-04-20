# Copilot Instructions for `agent_souls`

## Build, test, and lint commands

This repository currently has no configured build, test, or lint toolchain.

- **Build:** N/A
- **Test (full suite):** N/A
- **Test (single test):** N/A
- **Lint:** N/A

## High-level architecture

The repository is a canonical multilingual option catalog for defining an agent's "soul", split across three semantic dimensions:

- `personality_traits.json`: stable personality descriptors
- `communication_styles.json`: conversational/interaction style descriptors
- `work_attitudes.json`: workplace behavior descriptors

All three files share the same schema and are designed to be consumed together as parallel taxonomies:

```json
{
  "key": "snake_case_identifier",
  "aliases": {
    "en": "English",
    "zh": "中文",
    "ja": "日本語",
    "fr": "Français",
    "es": "Español",
    "de": "Deutsch"
  }
}
```

## Key conventions

- Keep `key` as the canonical identifier in `snake_case` (ASCII, stable, no spaces).
- Keep object field order as `key` then `aliases`.
- Keep each top-level array alphabetically sorted by `key`.
- Keep locale coverage consistent across files: `en`, `zh`, `ja`, `fr`, `es`, `de`.
- Keep aliases concise and label-like (not full-sentence descriptions).
