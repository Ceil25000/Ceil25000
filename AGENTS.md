# AGENTS.md

## Project overview

This repository is a **GitHub profile README** for [Ceil25000](https://github.com/Ceil25000/Ceil25000). The only source file is `README.md`, which GitHub renders on the user's profile page. There is no application server, database, build pipeline, or test suite in this repo.

## Cursor Cloud specific instructions

### Services

No services are required. There is nothing to start for local development beyond optional Markdown preview tooling.

### Lint

`README.md` intentionally uses inline HTML (`<picture>`, `<source>`, `<img>`) for light/dark mode images. Standard Markdown linters will report expected violations (for example `MD033/no-inline-html`). These are not bugs.

To lint anyway (informational only):

```bash
npx --yes markdownlint-cli2 "README.md"
```

### Preview (local hello-world)

To verify the README renders correctly:

```bash
mkdir -p /tmp/profile-preview
npx --yes marked -i README.md -o /tmp/profile-preview/index.html
python3 -m http.server 8765 --directory /tmp/profile-preview
```

Open http://127.0.0.1:8765/ and confirm the mascot image, "About me" section, and languages table (C++, Python, Rust) appear.

### Git workflow

Changes are made directly to `README.md` on `main` (or a feature branch). Commit and push to update the live GitHub profile after merge.

### Secrets and environment variables

None required for this repository.
