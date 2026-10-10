# Font Awesome component theme

The _Font Awesome_ component theme for [Cecil](https://cecil.app) provides helpers to use [Font Awesome icons](https://fontawesome.com/search?o=r&m=free&s=solid%2Cregular&f=brands%2Cclassic).

## Installation

```bash
composer require cecil/theme-fontawesome
```

> Or [download the latest archive](https://github.com/Cecilapp/theme-fontawesome/releases/latest/) and uncompress its content in `themes/fontawesome`.

## Usage

Add `fontawesome` in the `theme` section of the `config.yml`:

```yaml
theme:
  - fontawesome
```

Include styles and webfonts in the `<head>` of your template:

```twig
{{ include('partials/fontawesome.twig') }}
```

> By default, it includes _regular_, _solid_, and _brands_ icons, but you can select only the one(s) you want using the `styles` array, i.e.:
> `{{ include('partials/fontawesome.twig', {styles: ['brands']}) }}`

Then import macro in your template:

```twig
{% import 'macros/fontawesome.twig' as fontawesome %}
```

Display the desired icon:

```twig
{{ fontawesome.icon('<name>', '<style>', '<size>', '<rotate>', '<flip>', '<attributes>') }}
```

- `<name>`: name of the [icon](https://fontawesome.com/search?o=r&m=free&s=solid%2Cregular&f=brands%2Cclassic)
- `<style>`: style ("regular", "solid" or "brands". "regular" by default)
- `<size>`: font [size](https://fontawesome.com/docs/web/style/size) (optional)
- `<rotate>`: rotation in degrees ("90", "180", "270" or any custom angle, i.e. "45" or "-30")
- `<flip>`: flipping ("horizontal", "vertical" or "both")
- `<attributes>`: additional HTML attributes (optional, `aria-hidden="true"` by default)

## Example

```twig
{{ fontawesome.icon(name:'github', style:'brands', size:'xl', attributes:{style: 'color: #333'}) ~}}
```

```html
<i class="fa-brands fa-github fa-xl" aria-hidden="true" style="color: #333"></i>
```

## License

_Font Awesome_ component theme is a free software distributed under the terms of the MIT license.

Font Awesome Free is distributed under its own [license](https://fontawesome.com/license/free) (Icons: CC BY 4.0, Fonts: SIL OFL 1.1, Code: MIT License).
