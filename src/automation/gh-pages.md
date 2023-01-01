# GitHub Action for Pages

```yml
name: github pages

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v3

      - name: Read .env
        id: mdbook-version
        run: |
          . ./.env
          echo "::set-output name=MDBOOK_VERSION::${MDBOOK_VERSION}"

      - name: Setup mdbook
        uses: peaceiris/actions-mdbook@v1
        with:
          mdbook-version: '${{ steps.mdbook-version.outputs.MDBOOK_VERSION }}'

      - run: mdbook build

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./book
```

```yml
# .env
MDBOOK_VERSION=0.4.10
```

This is a configuration file for GitHub Actions that specifies a job that is run whenever a push is made to the main branch of the repository. The job consists of the following steps:

1. Check out the code from the repository.
2. Read the `.env` file and set the `MDBOOK_VERSION` environment variable to the value specified in the file.
3. Install `mdbook`, a tool for building documentation from Markdown files, with the version specified in the `MDBOOK_VERSION` environment variable.
4. Build the documentation using `mdbook`.
5. Deploy the built documentation to GitHub Pages using the `peaceiris/actions-gh-pages` action. The `GITHUB_TOKEN` secret is used to authenticate the action. The documentation is deployed from the ./book directory.

GitHub Pages is a static site hosting service provided by GitHub. This job will build and deploy the documentation to GitHub Pages, making it available to be viewed online.
