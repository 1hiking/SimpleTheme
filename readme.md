# SimpleTheme

![The words "Simple theme" with a white palette and bluish background](simpletheme.png)

A simple theme using the Nord palette. Currently it is focused on single-author blogs and no i18n support.

Some features:

- Automatic light and dark themes
- 100% only [Nord](https://www.nordtheme.com/) colors (Check [Theme Parameters](#theme-parameters) for code tags)
- [Open Graph](https://ogp.me/) support
- Support for favicons
- Support for vector (SVG) logos
- Table of contents and header anchors
- Automatic navigation for content (with some caveats)
- Support for [Image Processing](https://gohugo.io/content-management/image-processing/) without shortcodes (See [Images](#Images))
- PostCSS

## Quick installation

`git submodule add https://github.com/1hiking/SimpleTheme.git themes/SimpleTheme`
`cd themes/SimpleTheme` then `npm install`

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
footerText = "SampleText" # Any text you might want to display will go here.
logo = "/path/to/image" # Supports SVG.
logoalt = "My great logo" # alt description of the logo.

[author]
name = "example" # Name of the author.
github = "example" # https://github.com/example.

[markup]
  [markup.highlight]
    style = 'nord' # Add nord to match theme's palette
```

## Navigation caveats

To make a new section on the navigation bar, just make a new folder on /content/ and it will be picked up automatically.

Currently there are some issues:

- If you add a new section and delete it while executing `hugo serve` it won't remove it from the navigation bar

- If you add a \\\_index.md inside a content section, it will refuse to load. Currently this behavior is somewhat expected since they redirect to only lists.

## Adding a License

To add license as HTML, [override](https://gohugo.io/templates/lookup-order/) the `article-license.html` with a CC license for example, you could use the
[Creative Commons webpage](https://creativecommons.org/choose/)

## Shortcodes

You can add a Table of Content by adding the following line at the start of your article.

`{{< toc >}}`

You can define your own rendering on the [configuration file](https://gohugo.io/getting-started/configuration-markup#table-of-contents)

## Images

Images used on posts by default should be on /assets/ and not /static/. Furthermore, instead of using a simple `<img>` tag, we use a `<figure>`.

This is thanks to [Markup Render Hooks](https://gohugo.io/getting-started/configuration-markup#markdown-render-hooks) which means you can keep using the simple
`![]`

## Credits

Partial work of this page was taken from this [theme](https://github.com/qua3k/blog-theme)
