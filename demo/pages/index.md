---
title: Home
gallery: true
---
# Font Awesome for Cecil

This website is the demo of the [_Font Awesome_ component theme](https://github.com/Cecilapp/theme-fontawesome) for [Cecil](https://cecil.app): styles, webfonts and a Twig macro to display [Font Awesome Free](https://fontawesome.com/search?o=r&m=free) icons.

Include styles and webfonts in the `<head>`:

```twig
{{ include('partials/fontawesome.twig') }}
```

Then import the macro and display an icon:

```twig
{% import 'macros/fontawesome.twig' as fontawesome %}

{{ fontawesome.icon(name, style, size, rotate, flip, attributes) }}
```

- `style`: `regular` (default), `solid` or `brands`;
- `size`: `2xs`, `xs`, `sm`, `lg`, `xl`, `2xl` or `1x` to `10x` (optional);
- `rotate`: `90`, `180`, `270` or any custom angle, i.e. `45` or `-30` (optional);
- `flip`: `horizontal`, `vertical` or `both` (optional);
- `attributes`: additional HTML attributes (optional, `aria-hidden="true"` by default).

Icons are a font, so they follow the text color and size.
