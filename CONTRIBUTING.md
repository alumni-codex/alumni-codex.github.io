[mkd]: https://www.mkdocs.org/
[slk]: https://pivotal.fun/
[md]: https://www.markdownguide.org/
[mdr]: https://www.markdownguide.org/basic-syntax/#reference-style-links
[prs]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork

# Contributing to the Pivotal Alumni Codex

All pages are in [Markdown][md], so consult the [Markdown guide][md] for syntax.

## Editing Pages

Feel free to edit any existing page. We have a _slight_ preference for [reference-style links][mdr] at the top of a page for readability.

## Adding Pages

When adding a new page please keep in mind a few things.

- All files must be valid Markdown syntax and end in the `.md` extension
- Files in the `/docs` directory will show up in the root
  - e.g., `/who_is_ora.md` will build a page at `https://alumni-codex.github.io/who_is_ora/`
- If you want to make a collection of related pages
  - Create a new directory under `/docs`
    - e.g., `/docs/pivotal_breakfast/`
  - Create new pages underneath your new directory and write those pages
    - `/docs/pivotal_breakfast/ora.md` and `/docs/pivotal_breakfast/gemma.md`; these will render to `https://alumni-codex.github.io/pivotal_breakfast/ora/` and `https://alumni-codex.github.io/pivotal_breakfast/gemma/` respectively
    - `/docs/pivotal_breakfast/index.md/` will render to `https://alumni-codex.github.io/pivotal_breakfast/`

### Adding New Pages to Nav

Whenever you add new pages, you need to _add them to the left-side navigation __manually___. 

To add these new pages, you need to update the `nav` section of `mkdocs.yml`. Use the existing file as a guide.

## Local Development

Please fork the repo for local development. See below re: Pull Requests.

All of the source to this site is in the `main` branch in the `/docs` directory. This directory and its subdirectories adhere to [MkDocs][mkd] patterns.

Local development is _not required_, but it can help maintainers get your edits to the web faster.

### Setup
To set up a local development environment - that is, to allow for live reload and preview of the built HTML - you will need:

- Homebrew
- Python 3 + `pip`

```bash
brew bundle # see the Brewfile in the repo root
pip3 install -r requirements.txt
mkdocs server
# make changes to docs (see below)
# make sure markdown formatted correctly
deno fmt .
# make git commit and PR (optional)
```
## Submitting a Pull Request

We're using GitHub's PR flow to manage contributions and deal with potential conflicts.

If you're not familiar with how Pull Requests work. Here's the TL/DR.

Once your changes are ready:

- Commit your changes locally
- Push to GitHub
- Create a PR from your fork back to the main
    - If necessary, GitHub has this [guide][prs]

Most PRs will be accepted without fuss. But we do want to keep the site well organized. So we might have some questions and/or suggest pairing before merging.
