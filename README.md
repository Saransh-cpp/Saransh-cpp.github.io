# Website

[![pages-build-deployment](https://github.com/Saransh-cpp/Saransh-cpp.github.io/actions/workflows/pages/pages-build-deployment/badge.svg?branch=master)](https://github.com/Saransh-cpp/Saransh-cpp.github.io/actions/workflows/pages/pages-build-deployment)

My personal website.

## Running locally

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system:

```bash
$ git clone git@github.com:Saransh-cpp/Saransh-cpp.github.io.git
$ cd Saransh-cpp.github.io
$ bundle install
$ bundle exec jekyll serve
```

The source code is on the `source` branch and the website is generated on the `master` branch.
The folders on the `source` branch are self-explanotary (for me).

## Deployment

Deployment is managed via GitHub Pages and is triggered on every push to `master`.
However, to manually re-deploy the website, run the deploy script from the root directory:

```bash
$ ./bin/deploy --user
```

which uses the `source` branch for the source code and deploys the webpage.

## Atom (RSS-like) Feed
An Atom (RSS-like) feed of my posts, useful for Atom and RSS readers -
[/feed.xml](https://saransh-cpp.github.io/feed.xml).

## License

Based on [al-folio](https://github.com/alshedivat/al-folio) theme, by [Maruan Al-Shedivat](https://maruan.alshedivat.com)
under the MIT license. However, I have customized the theme to match my personal needs.
