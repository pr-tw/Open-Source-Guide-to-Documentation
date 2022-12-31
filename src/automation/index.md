# Automation

Just like with code releases, documentation can benefit from using the same tools for automating.

Automation and documentation tools can also help you streamline the documentation process.

## CI/CD

Continuous integration, continuous delivery, and continuous deployment workflows can be used for documentation site. This can help ensure that your documentation is always up-to-date and accurate, and that any changes are quickly tested and deployed.

Continuous integration can automate processes such as running tests and builds, while continuous delivery and deployment can automate the process of releasing updates to your documentation. This can help speed up the process of releasing updates, as well as make it easier to track and troubleshoot any issues that arise.

It's important to consider the needs of your documentation when selecting the appropriate tools for your workflow. Look for tools that have good documentation and support, and make sure they can handle the complexity of your project. Additionally, make sure that the cost of the tools is worth the features and capabilities they provide.

## Tests and other checks

You can run tests on your documentation in a GitHub repo or other to check for broken links or even code samples.

### Testing links

There are a variety of GitHub Actions that you can run on your repositories documentation or pull requests, which can help contributors feel confident that they won’t break anything.

### Testing code samples

There isn't a one-size-fits-all solution to test code samples in documentation. Depending on the coding language and documentation framework you choose will determine the solution you use to test code samples in your documentation.

For example, you can test Rust code with [mdbooks](https://rust-lang.github.io/mdBook/cli/test.html); however, at the time of this writing, no other languages are tested by default.
