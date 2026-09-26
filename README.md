# new.css

A classless CSS framework to write modern websites using only HTML. It weighs **4.8kb**.

All it does is set some sensible defaults and styles your HTML to look reasonable. It's perfect for:

- A dead-simple blog
- Collecting your most used links
- Making a simple "about me" site
- Rendering markdown-generated HTML

**Demo: [newcss.net](https://newcss.net/)**

---

## Usage

### HTML

Add this line to the end of your HTML's `<head>`:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1/new.min.css">
```

If you'd like the font [Inter](https://rsms.me/inter) as well (recommended), add this line as well:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/open-fonts@1.1.1/fonts/inter.min.css">
```

### npm

```shell
npm i @exampledev/new.css
```

### Yarn

```shell
yarn add @exampledev/new.css
```

## Themes

new.css uses a color palette that can be easily customized. These are declared as a CSS variable in the :root attribute.

### Theme Library

See pre-made themes at [newcss.net/themes](https://newcss.net/themes/).

### Customizing Themes

Information is available [on the wiki](https://github.com/xz/new.css/wiki/Customizing-Themes).

## FAQ

**Why should I use this instead of (popular framework)?**

new.css wasn't made to be a true framework. It's made for rapidly prototyping your raw HTML or setting up a good-looking simple HTML site with zero configuration.

**Does this work with (platform/service)?**

new.css was designed to work with nothing but raw HTML, but some awesome community members are porting it to other platforms. 

Check if your platform or service supports custom CSS. If it does, it'll probably work. You're welcome to [ask the community](https://discord.gg/hhuuC4w) as well.

## Special Thanks
- [sakura by oxal](https://github.com/oxalorg/sakura) for introducing me to classless CSS
- [mydarkstar](https://mydarkstar.net/) for priceless advice
