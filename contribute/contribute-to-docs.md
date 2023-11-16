# CONTRIBUTE TO DOCS

## Contributors Guide

This page will go into detail on how to contribute to the Pocket Network documentation site at [https://docs.pokt.network](https://docs.pokt.network). If you are familiar with Markdown and contributing to an open-source repo on GitHub, the quick setup section may be all you need.

### Required installations

To contribute to the documentation, you only need one tool:

1. [Git](https://git-scm.com/)

#### Install Git

**Windows**

Download and install the corresponding [Git for Windows](https://git-scm.com/download/win) setup for your system, either 32- or 64-bit.

**Mac**

From a terminal, run:

```sh
git --version
```

If it's not installed, you'll be prompted with an installer.

### Making changes

#### Editing existing pages

To edit an existing page, open a Markdown file in a text editor, make your changes, and save the file.

#### Adding pages to existing sections

If you want to add content, create a new markdown file in the appropriate directory. Each file needs a front matter specifying `title`, `menuTitle`, `weight`.

Here's an example of the front matter for a Glossary page:

```yaml
---
title: Glossary
menuTitle: Glossary
weight: 10
---
```

After the front matter, you can create the rest of the content in Markdown.

#### Adding new sections

To add a new section, create a new directory under the appropriate location and add an `_index.md` file. You can also add any additional markdown files in that directory, as needed.

### Contributing via Git

To contribute changes:

1. Clone the repository to your local machine.
2. Make your changes in the appropriate files or directories.
3. Commit your changes and push them to your fork of the repository.
4. Create a pull request against the main repository with your changes.

For more detailed instructions on using Git, refer to the [official Git documentation](https://git-scm.com/doc).
