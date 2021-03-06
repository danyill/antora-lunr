# Antora Site Generator With Lunr

[![npm](https://img.shields.io/npm/v/antora-site-generator-lunr)](https://www.npmjs.com/package/antora-site-generator-lunr)

This site generator is a copy of the [default site generator](https://gitlab.com/antora/antora/blob/master/packages/site-generator-default/README.adoc) that in addition produces a Lunr index that can be used in your documentation UI.
Lunr provides a great search experience in your documentation site without the need for external, server-side, search services.

[Antora](https://antora.org) is a modular static site generator designed for creating documentation sites from AsciiDoc documents.
Its site generator pipeline aggregates documents from versioned content repositories and processes them using [Asciidoctor](https://asciidoctor.org).

## Usage

Install the site generator.
Open a terminal and type:

    $ npm i -g antora-site-generator-lunr

When generating your documentation site, use the `--generator` option:

    $ DOCSEARCH_ENABLED=true DOCSEARCH_ENGINE=lunr NODE_PATH="$(npm -g root)" antora --generator antora-site-generator-lunr site.yml

**NOTE:** The `NODE_PATH` assignment is necessary to ensure Antora can locate node modules install globally.
Depending on your environment, you may find that this assignment is unnecessary.
If you've installed Antora globally using Yarn, you may need to add `"$(yarn global dir)/node_modules"` to the `NODE_PATH` environment variable instead.

Please read the [documentation](https://github.com/Mogztter/antora-lunr#enable-the-search-component-in-the-ui) to enable the search component in your documentation UI.
