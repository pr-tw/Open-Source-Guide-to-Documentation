# Advanced topics

The following discuss advanced topics of managing documentation.

## Creating and maintaining a documentation website

Users generally interact with your documentation through a web server. Finding a way to host and serve your documentation can be tricky.
You will need to find a static site generator and a server to host the documentation.

### Static site generators

Static site generators generate full HTL websites based on a set of templates. There are many static site generators. In fact, [Jamstack](https://jamstack.org/generators/) contains a list of static site generators that can be configured for Jamstack sites.

The following are highlighted static sites:

- [Mdbook](https://rust-lang.github.io/mdBook/index.html)
- [Hugo](https://gohugo.io)
- [Docusaurus](https://docusaurus.io)

### Hosting documentation

[GitHub pages](https://pages.github.com) can host websites directly from your GitHub repository. You can manage your documentation repo just like you would any other code and make edits and releases.

[Read the Docs](https://docs.readthedocs.io/en/stable/) also simplifies hosting your documentation and offers its servers for free. The advantage of Read the Docs, is that your documentation can live on GitHub, BitBucket, or GitLab.

#### Paid services

If you're maintaining documentation for a large business, you may want to look at paid options like [Netlify](https://www.netlify.com) or [Vercel](https://vercel.com/).

## Using documentation tools and automation

The use of linters, spellcheckers, and formatters are a great set of tools to use against your documentation.

### Linters

Just like with code, you can lint your prose for issues.
Linters like [alexjs](https://alexjs.com) can be used to catch insensitive or inconsiderate writing.

More complex linters like [Vale](https://vale.sh) allow you to create your own rules or use existing style guides to enforce writing standards.

### Spellcheckers

There are a variety of spellcheckers and can be used at any stage of the writing process.
Consider adding a spellchecker to your text editor. For example, VS Code has a Markdown spellchecker from [LanguageTool,](https://marketplace.visualstudio.com/items?itemName=adamvoss.vscode-languagetool) which provides offline grammar checking in VS Code using a local server.

### Formatters

While the line between linters and formatters is thin, some formatters like [Prettier](https://prettier.io) and [dprint](https://dprint.dev) can format and lint markdown files and even code blocks. Formatters aren't a one size fits all solution. For example, Prettier doesn't work for Python code blocks. You'd have to use a formatter like [blacken-docs](https://github.com/adamchainz/blacken-docs) which runs the [black](https://black.readthedocs.io/en/stable/) formatter on code blocks.

Formatting is useful so that you have consistency throughout your docs and check for specific errors.
