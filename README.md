[fun]: https://pivotal.fun/codex
[direct]: https://alumni-codex.github.io/
[mkd]: https://www.mkdocs.org/
[slk]: https://pivotal.fun/
[contrib]: ./CONTRIBUTING.md

# The Pivotal Alumni Codex

A place for the links to the things we wish we'd taken with us. Hosted at GitHub at https://alumni-codex.github.io/ and as a redirect from https://pivotal.fun/codex. 

Given that the [Pivotal Alumni Slack][slk] is free, and free Slacks have only 90-day retention, we use this site to bookmark web stuff that we find helpful _after_ Pivotal.

- The `main` branch of this repo the source code for this site
- When changes are made to the `main` brach, GitHub Actions builds and deploys HTML
- The HTML and CSS are generated with [MkDocs][mkd]
- This site is hosted via GitHub Pages

## Contributing

- All changes should come via Pull Request.
- Please see [CONTRIBUTING.md][contrib] for details on how to add and update files.
- Be Kind
- Reach out to Davis - @infews - if you want to help with admin of this site

## Development

You will need Python 3 and the Pip package manager.

```bash
# Install dependencies
pip install -r requirements.txt
# Run the dev server
mkdocs serve
# Navigate your browser to it
open http://127.0.0.1:8000/
```
