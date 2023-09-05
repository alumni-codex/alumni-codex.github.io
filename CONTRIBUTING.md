[mkd]: https://www.mkdocs.org/
[slk]: https://pivotal.fun/
[md]: https://www.markdownguide.org/
[mdr]: https://www.markdownguide.org/basic-syntax/#reference-style-links

# Contributing to the Pivotal Alumni Codex

## What should I contribute?

Anything Pivotal practices and tips/tricks!

We are using a pull request flow for this site. So please fork, write/edit, and the submit a PR to this repo for review.

All pages are [Markdown][md], so consult the [guide][md] for syntax.

## Editing Pages

Feel free to edit any existing page. We have a _slight_ preference for [reference-style links][mdr] at the top of a page for readability.

## Adding Pages

When adding a new page please keep in mind a few things.

- All files must be valid Markdown syntax and end in the `.md` extension
- Files in the `/docs` directory will show up in the root
  - e.g., `who_is_ora.md` will build a page at `https://alumni-codex.github.io/who_is_ora/`
- If you want to make a collection of related pages
  - Create a new directory under `/docs`
    - e.g., `/docs/pivotal_breakfast/`
  - Create new pages underneath your new directory and write what you need to
    - e.g., `/docs/pivotal_breakfast/ora.md` and `/docs/pivotal_breakfast/gemma.md`; these will render to `https://alumni-codex.github.io/pivotal_breakfast/ora/` and `https://alumni-codex.github.io/pivotal_breakfast/gemma/` respectively

### Adding New Pages to Nav

Whenever you add new pages, you need to _add them to the left-side navigation manually_. 

To add these new pages, you need to update the `nav` section of `mkdocs.yml`. Use the existing file as a guide.

## Local Development

All of the source to this site is in the `main` branch in the `/docs` directory. This directory and its subdirectories adhere to [MkDocs][mkd] patterns.

Local development is _not required_, but it can help maintainers get your edits to the web faster.

To set up a local development environment - that is, to allow for live reload and preview of the built HTML - you will need:

- Homebrew
- Python 3 + `pip`

```bash
brew bundle
pip3 install -r requirements.txt
mkdocs server
# make changes to docs (see below)
# make sure markdown formatted correctly
deno fmt .
# make git commit and PR
```