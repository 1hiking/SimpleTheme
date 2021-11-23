# SimpleTheme

A simple theme using the Nord palette (for the most part). Currently it is
focused on single-author blogs and no i18n support.

## Theme parameters

```TOML
baseURL = "https://example.com"
languageCode = "en-us" # Language will defined on meta.
relativeURLs = true
title = "Example Site"
theme = "SimpleTheme"
sectionPagesMenu = "main" # Enables automatic navigation bar.

[params]
dateFormat = "02 of January of 2006" # How the date will be displayed on posts.
copyright = "1hiking" # Will be displayed on Footer.
logo = "/path/to/image" # Supports SVG.
logoalt = "My great logo" # alt description of the logo.

[author]
name = "example" # Name of the author.
github = "example" # https://github.com/example.
```

## Shortcodes

You can add a Table of Content by adding the following line at the start of your
article.

`{{< toc >}}`

You can define your own rendering on the
[configuration file](https://gohugo.io/getting-started/configuration-markup#table-of-contents)

## Credits

Partial work of this page was taken from this
[theme](https://github.com/qua3k/blog-theme)
