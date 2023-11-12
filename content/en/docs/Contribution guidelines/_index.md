---
title: Contribution Guidelines
weight: 10
description: How to contribute to the ssentezo Wallet API documentation.
---

{{% pageinfo %}}
These contribution guidelines assume that your Docsy site is deployed using Netlify and your files are stored on GitHub. You can adapt them with your own instructions based on your deployment options, file structure, project-specific review guidelines, versioning guidelines, or any other information your users might find useful when updating your site.
{{% /pageinfo %}}

## Contributing to ssentezo Wallet API Documentation

Thank you for considering contributing to the ssentezo Wallet API documentation. Your contributions help improve the quality and usefulness of our documentation.

### Submission Process

All contributions, including those from project members, require review. We use GitHub pull requests (PRs) for this purpose. If you're new to GitHub pull requests, consult [GitHub Help](https://help.github.com/articles/about-pull-requests/) for more information on using pull requests.

### Quick Start with Netlify

Here's a quick guide to updating the documentation. It assumes you're familiar with the GitHub workflow and you're happy to use the automated preview of your doc updates:

1. Fork the [ssentezo-wallet-docs repository](https://github.com/ssentezo/ssentezo-wallet-docs) on GitHub.
2. Make your changes and send a pull request (PR).
3. If you're not yet ready for a review, add "WIP" to the PR name to indicate it's a work in progress. (**Don't** add the Hugo property "draft = true" to the page front matter, because that prevents the auto-deployment of the content preview described in the next point.)
4. Wait for the automated PR workflow to perform some checks. When it's ready, you should see a comment like this: **deploy/netlify — Deploy preview ready!**
5. Click **Details** to the right of "Deploy preview ready" to see a preview of your updates.
6. Continue updating your doc and pushing your changes until you're happy with the content.
7. When you're ready for a review, add a comment to the PR and remove any "WIP" markers.

### Updating a Single Page

If you've just spotted something you'd like to change while using the docs, Docsy has a shortcut for you:

1. Click **Edit this page** in the top right-hand corner of the page.
2. If you don't already have an up-to-date fork of the project repo, you are prompted to get one - click **Fork this repository and propose changes** or **Update your Fork** to get an up-to-date version of the project to edit. The appropriate page in your fork is displayed in edit mode.
3. Follow the rest of the [Quick Start with Netlify](#quick-start-with-netlify) process above to make, preview, and propose your changes.

### Previewing Your Changes Locally

If you want to run your local Hugo server to preview changes as you work:

1. Follow the instructions in [Getting Started](/docs/getting-started) to install Hugo and any other tools you need. You'll need at least **Hugo version 0.45** (we recommend using the most recent available version), and it must be the **extended** version, which supports SCSS.
2. Fork the [ssentezo-wallet-docs repository](https://github.com/ssentezo/ssentezo-wallet-docs) into your own project, then create a local copy using `git clone`. Don’t forget to use `--recurse-submodules` or you won’t pull down some of the code you need to generate a working site.

   ```bash
   git clone --recurse-submodules --depth 1 https://github.com/ssentezo/ssentezo-wallet-docs.git
