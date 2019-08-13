# Linked Data Fragments website
This repository contains the source code for [linkeddatafragments.org](https://linkeddatafragments.org).

## Adding publications
The publications list is automatically generated from BibTeX. You can add your work on Linked Data Fragments by:
- adding a BibTeX entry to [assets/publications/publications.bib](https://github.com/LinkedDataFragments/Website/blob/master/assets/publications/publications.bib)
- adding the key of your BibTeX entry to [content/publications.md](https://raw.githubusercontent.com/LinkedDataFragments/Website/master/content/publications.md)

Please follow the formatting of the other BibTeX entries.

## Compiling the site locally
This site uses the [Nanoc static site compiler](https://nanoc.ws/).

### Preparations
- Install Ruby >= 2.2.5 and the bundler gem
- `git clone https://github.com/LinkedDataFragments/Website.git`
- `cd Website`
- `bundle install`

### Compilation
- one-time: `bundle exec nanoc compile`
- continuous: `bundle exec guard`
