# SimpleTheme

![The words "Simple theme" with a white palette and bluish background](simpletheme.png)

A simple theme using the Nord palette. Currently it is focused on single-author blogs and no i18n support.

Some features:

- Automatic light and dark theme
- [Nord based colors](https://www.nordtheme.com/) colors (Check [Theme Parameters](#theme-parameters) for code tags)
- [Open Graph](https://ogp.me/) support
- Support for favicons
- Support for vector (SVG) logos
- Table of contents and header anchors
- Support for navigation headers
- Support for [Image Processing](https://gohugo.io/content-management/image-processing/) without shortcodes (See [Images](#Images))

## Quick installation

`git submodule add https://github.com/1hiking/SimpleTheme.git themes/SimpleTheme`


## Theme parameters

```TOML
baseURL = "https://example.com"
languageCode = "en-us" # Language will defined on meta.
relativeURLs = true
title = "Example Site"
theme = "SimpleTheme"
sectionPagesMenu = "main" # Enables automatic navigation bar.

[menu]
# https://gohugo.io/content-management/menus/
[[menu.main]]
identifier = "About"
name = "About"
url = "/about/"
weight = 10

[[menu.main]]
homepage = "Posts"
name = "Posts"
url = "/posts/"
weight = 10

[params]
dateFormat = "02 of January of 2006" # How the date will be displayed on posts.
copyright = "1hiking" # Will be displayed on Footer.
logo = "/path/to/image" # Supports SVG.
logoalt = "My great logo" # alt description of the logo.
postCSS = true # For postCSS support.

[author]
name = "example" # Name of the author.
github = "example" # https://github.com/example.

[markup]
  [markup.highlight]
    style = 'nord' # Add nord to match theme's palette
```

## Adding a License

To add license as HTML, [override](https://gohugo.io/templates/lookup-order/) the `article-license.html` with a CC license for example, you could use the
[Creative Commons webpage](https://creativecommons.org/choose/)

## Custom Shortcodes

You can add a Table of Content by adding the following line at the start of your article.

`{{< toc >}}`

You can define your own rendering on the [configuration file](https://gohugo.io/getting-started/configuration-markup#table-of-contents)

## Credits

Partial work of this page was taken from this [theme](https://github.com/qua3k/blog-theme).
