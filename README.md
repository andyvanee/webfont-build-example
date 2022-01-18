# webfont-build-example

Example repo to test building webfont with github actions

`bin/generate-fonts.js` includes some hardcoded paths which would need to be
changed if you want to move things around.

### `icons/template.css`

This file is used as a template to generate the CSS file to load the font
in the browser.

`__VERSION__` will be replaced with an actual version number on build.

`/* ICON_VARS */` comment will be replaced with CSS variable declarations, which
can be used if you want to reference the icons within web components, or other
stylesheets.

```css
:root {
    --icon-content-facebook: "\e001";
}

/* later */

.my-icon-class {
    font-family: "webfont";
    content: var(--icon-content-facebook);
}
```

`/* ICONS */` comment will be replaced with the actual icon definitions.

### `icons/template.html`

This file is used as a template to generate a preview of the font.

`__VERSION__` will be replaced with an actual version number on build.

`<!-- ICONS -->` comment will be replaced with the HTML to render each icon in
the browser.
