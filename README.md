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

Import macro in your template:

```twig
{% import 'macros/fontawesome.twig' as fontawesome %}
```

Then include styles and webfonts in the `<head>` of your template:

```twig
{% include 'partials/fontawesome.twig' %}
```

Display the desired icon:

```twig
{{ fontawesome.icon('<name>', '<style>', '<size>', '<attributes>') }}
```

- `<name>`: name of the [icon](https://fontawesome.com/search?o=r&m=free&s=solid%2Cregular&f=brands%2Cclassic)
- `<style>`: style ("regular", "solid" or "brands", "regular" by default)
- `<size>`: font [size](https://fontawesome.com/docs/web/style/size) (optional)
- `<attributes>`: additional HTML attributes (optional)

## Example

```twig
{{ fontawesome.icon('github', 'brands', 'xl', {style: 'color: #333'}) ~}}
```

```html
<i class="fa-github fa-brands fa-xl" style="color: #333">
```
