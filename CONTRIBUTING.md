# Contributing

## Adding a prompt

1. Pick the matching category folder under `prompts/`, `templates/`, `guides/`, `techniques/`, `agents/`, or `packs/`. If none fits, open an issue first instead of adding a new top-level folder.
2. Name the file in lowercase kebab-case with a `.md` extension, for example `my-new-prompt.md`.
3. Add frontmatter at the top, with `title`, `category`, `models`, `use_case`, and `updated`. Leave `models` and `updated` blank when the source does not state them. Do not invent a model or a date.
4. Keep the prompt text copy-paste ready. Do not rewrite other prompts in the same change.
5. Add one row to [CATALOG.md](CATALOG.md) and to the category README.

## Fixing something

Open an issue or a pull request. For a broken link, a wrong path, or a typo, a pull request with only that fix is welcome. For a duplicate or a file to remove, open an issue first and name the file, so the removal is a recorded decision.

## Style

- Relative links only, for example `[Marketing prompts](prompts/marketing/marketing-prompts.md)`.
- No deeper than three levels: category folders hold files, not further subfolders, except `templates/xml/`.
- Keep each file self-contained. Images go in `assets/` and are linked relatively.
