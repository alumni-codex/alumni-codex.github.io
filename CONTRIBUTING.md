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
- Every file needs YAML front matter that looks like this:

```yaml
---
title: <My new page title>
layout: default # so that the side nav renders on this page
parent: <title of parent page> # puts this page in the side nav
---
```

- In order to be connected to the side navigation, the file needs a `parent` (see above)
  - e.g., `/who_is_ora.md` will build a page at `https://alumni-codex.github.io/who_is_ora/`
- New Directories are welcome!
  - The directory needs an `index.md` for this group of related pages 
  - This `index.md` doesn't need a parent, but it needs a `nav_order: integer` to place it in the Side Nav 

## Local Development

Please fork the repo for local development. See below re: Pull Requests.

All of the source to this site is in the `main` branch directory. This directory and its subdirectories adhere to [Jekyll](https://jekyllrb.com) patterns.

Local development is _not required_, but it can help maintainers get your edits to the web faster.

### Setup
To set up a local development environment - that is, to allow for live reload and preview of the built HTML - you will need:

- Homebrew (to install a useful Ruby)
- Ruby 3.3.x and Bundler
- 
## Development

You will need Ruby 3.3.x and Bundler in order to validate locally.

```bash
# Install dependencies
bundle install
# Run the dev server
bundle exec jekyll serve
# Navigate your browser to it
open http://127.0.0.1:4000/
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
