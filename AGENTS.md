# Agent instructions

This is Andrew Baisden's GitHub profile repository. `README.md` is rendered on the GitHub profile page, and `img/` holds its images. There is no application code, build, or test suite.

## Before you change anything

- Run `git pull` before editing any file. Scheduled GitHub Actions commit to this repository (see below), so a stale checkout causes merge conflicts.
- Make changes only when asked, and keep them to what was asked. Do not reword, reorder, or restyle other sections.

## Commits

- Use [Conventional Commits](https://www.conventionalcommits.org/): `type: summary` in the imperative mood, for example `docs: add IssueRelay featured project` or `chore: remove unused header image`. Use `docs` for README content, `chore` for images and housekeeping, and `ci` for workflow changes.
- Keep one logical change per commit, and never commit `.DS_Store` or other local files.
- Commit and push only when the owner asks.

## README structure

- Keep the existing section order: header image, name and links, About, Featured Projects, Tech Stack, Engineering Focus, Currently, Technical Writing, GitHub stats, Connect. Sections are separated by `---`.
- **Featured projects:** the newest project goes **first**. Each one follows the same pattern:
  1. `### <emoji> <Project name>`
  2. `![<Project name>](img/<name>.png)`
  3. One paragraph: the problem, then **<Project name>** is … with the key features in bold.
  4. `Built with **Next.js** as a modern way to …`
  5. `Tech stack: **A · B · C**` using `·` separators.
  6. `→` links: `Live Demo` or `npm Package` (if there is one), then `Source Code`, joined with ` · `.
  7. A `---` separator after the project.
- When a project introduces a technology, add it to the matching Tech Stack line if it is not already there.
- Do not edit anything between `<!-- BLOG-POST-LIST:START -->` and `<!-- BLOG-POST-LIST:END -->`. The `blog-post-workflow.yml` Action rewrites that list every hour from the DEV feed.

## Images

- Save project images in `img/` as PNG, named after the project in lowercase without spaces (for example `img/issuerelay.png`).
- Match the existing images: a landscape capture of the project's home page or main screen, about 2500 × 1600 pixels (a 2x retina capture).
- Screenshots must never show real email addresses, passwords, API keys, tokens, or private user data. Use demo or seeded data.
- Delete an image when the README no longer uses it.

## Workflows

- `.github/workflows/blog-post-workflow.yml` updates the Technical Writing list from the DEV feed.
- `.github/workflows/main.yml` generates the contribution snake graphic.
- Change workflows only when asked.

## Links and content

- Check that every new link works before committing.
- Keep claims accurate: link only to live demos and packages that exist, and use tech stack entries the project actually uses.
