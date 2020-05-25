# new.css

**[newcss.net](https://newcss.net) / [xz Discord](https://discord.gg/hhuuC4w)** / **[Twitter](https://twitter.com/example_dev)**

A classless CSS framework to write modern websites using only HTML. It weighs **~4.5kb**.

Take a look at the demo on [newcss.net](https://newcss.net/), or the quick-start guide on [newcss.net/usage](https://newcss.net/usage/). It's on npm as `@exampledev/new.css`.

[Vercel](https://vercel.com?utm_source=xz&amp;utm_campaign=new.css)'s impossibly fast CDN delivers the font [Inter](https://rsms.me/inter) using [xz/fonts](https://github.com/xz/fonts), so there's virtually no bloat added to your pages.

And of course, there's a dark mode. It automatically applies a light/dark theme based on your browser's preference.

It supports custom color themes and fonts using CSS variables. For example, check out the terminal theme: [newcss.net/theme/terminal/](https://newcss.net/theme/terminal/)

new.css is a project from [xz](https://xz.style).

## Table of Contents
- [Usage](#usage)
- [Use Cases](#use-cases)
- [Details](#details)
- [Themes](#themes)
    - [Customizing](#customizing)
    - [Legend](#legend)
    - [Usage](#usage)
- [Pre-made Themes](#pre-made-themes)
    - [Night](#night)
    - [Terminal](#terminal)
- [Special Thanks](#special-thanks)


## Usage

Here's your configuration:

### HTML

Add this code to the end of your `<head>`:
```html
<link rel="stylesheet" href="https://fonts.xz.style/serve/inter.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
```

<br>

> 💡 new.css is best with the font [Inter](https://rsms.me/inter), which the line above imports as well. Use this line instead if you prefer no added fonts:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
```

### npm

Or, if you prefer npm:

1. `npm i @exampledev/new.css`

### yarn

With Yarn:

1. `yarn add @exampledev/new.css`

## Use Cases
- A dead-simple blog
- Collecting your most used links
- Making a simple "about me" site
- Rendering markdown-generated HTML

## Details
### Element Guide
How to use some of new.css' semantic HTML features.

- `button`
    - Wrap a button in an `<a>` tag to make it a link.
- Code
    - For inline code, use `<code>`.
    - For code blocks, use `<pre>`.
    - For keyboard input, use `<kbd>`,
    - There's no reason to nest code tags inside each other, however, `<code>` and `<pre>` will reset themselves to match if you nest them.
- `header`
    - **Only use a `<header>` at the top of your `<body>`!**
    - Creates a large and slightly darker header.

Here are the improvements new.css adds to your browser's basic HTML.

<details>
<summary>Full Changes</summary>

- **Global**
    - Slightly increase all text sizes
    - Use a less harsh color scheme
    - Use the Inter font, and if not possible, the system font
    - Redefine all margins to more sensible defaults
- `body`
    - Set a reasonable max width
    - Centered the body element, keeping left-alignment
- `abbr`
    - Question mark cursor on hover
- `blockquote`
    - Improved margins
    - Added background color
- `button`
    - Appears uniformly across browsers
    - Looks like a real button
- `code`
    - Added background color
    - Added outline stroke
- `details`
    - Looks more button-like with background color and link cursor on hover
- `h1`–`h6`
    - Uniform margins and padding
    - Tweaked font size
- `h1-h3`
    - Added thin bottom border line
- `hr`
    - Changed to single 1px line
- `kbd`
    - Looks like a real keyboard key
- `mark`
    - Added padding
    - Color follows theme
- `nav`
    - Added between-element margins
- `samp`
    - Ambiguous element, merged with `code`
- `table`
    - Basic styling to make cells more discernable
        - Border stroke across all cells
        - Alternating row background color
</details>

## Themes
new.css uses an 10-color palette and can be easily customized. These are declared as a CSS variable in the `:root` attribute.

### Customizing

By loading a secondary style sheet after new.css in your HTML, you can override these variables. Here's the default theme:

<details>
<summary>Default theme</summary>

```css
@import url('https://fonts.xz.style/serve/inter.css');

:root {
	--nc-font-sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
	--nc-font-mono: 'Courier New', Courier, 'Ubuntu Mono', 'Liberation Mono', monospace;
	--nc-tx-1: #000000;
	--nc-tx-2: #1A1A1A;
	--nc-bg-1: #FFFFFF;
	--nc-bg-2: #F6F8FA;
	--nc-bg-3: #E5E7EB;
	--nc-lk-1: #0070F3;
	--nc-lk-2: #0366D6;
	--nc-lk-tx: #FFFFFF;
	--nc-ac-1: #79FFE1;
    --nc-ac-tx: #0C4047;
}
```
</details>

### Legend

- `--nc-font-sans`: Font for all text besides code or preformatted
- `--nc-font-mono`: Font for `<code>`, `<pre>`, `<kbd>`, `<samp>`
- `--nc-tx-1`: Heading text color
- `--nc-tx-2`: Body text color
- `--nc-bg-1`: Base background color
- `--nc-bg-2`: Slightly darker background color
- `--nc-bg-3`: Even slightly darker background color
- `--nc-lk-1`: Action color for links and buttons
- `--nc-lk-2`: Link and buttons on mouse hover and active
- `--nc-ac-1`: Accent color for `<mark>` and text selection background

### Usage
1. Create a stylesheet including some or all of the above variables in the `:root`. An example theme file is available here: [boilerplate.css](https://newcss.net/theme/boilerplate.css)
2. If you'd like to import custom fonts, put the `@import` tag before the `:root` element. Many open-source fonts are available on [xz/fonts](https://github.com/xz/fonts).
3. Reference your new stylesheet **after** new.css in your `<head>`. Here's an example `<head>`:
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.3/new.min.css">">
    <link rel="stylesheet" href="https://example.com/MY-CUSTOM-THEME.css">
</head>
```

## Pre-Made Themes
Here are two extra themes with CDN links. Feel free to use or edit them!

### Night
```html
<link rel="stylesheet" href="https://newcss.net/theme/night.css">
```

Preview at [newcss.net/theme/night/](https://newcss.net/theme/night/)

<img src="https://newcss.net/_assets/night.png" alt="Night theme" width="300px">

### Terminal
```html
<link rel="stylesheet" href="https://newcss.net/theme/terminal.css">
```

Preview at [newcss.net/theme/terminal/](https://newcss.net/theme/terminal/)

<img src="https://newcss.net/_assets/terminal.png" alt="Terminal theme" width="300px">

## Sponsors
- <a href="https://domaincord.org/?utm_source=xz&utm_campaign=new.css">Domaincord</a> (also a domain name discussion group <a href="https://discord.gg/239EP7G">here</a>!)
- <a href="https://vercel.com/?utm_source=xz&utm_campaign=new.css">Vercel</a>

## Special Thanks
- [sakura by oxal](https://github.com/oxalorg/sakura) for introducing me to classless CSS
- [mydarkstar](https://mydarkstar.net/) for priceless advice
- [Vercel](https://vercel.com/?utm_source=xz&utm_campaign=new.css) for sponsoring [xz](https://xz.style) and for their amazing color palettes

<br>
<hr>
<br>

<a href="https://vercel.com?utm_source=xz&amp;utm_campaign=new.css" target="_blank"><img src="https://vercel-badges.now.sh/powered-by-vercel.svg" alt="Powered by Vercel"></a>
