# Bcredi - CSS Style

## Basic Rules
1. Two *spaces* for indentation
2. One rule per line
3. One selector per line
4. Space between rules and brackets
5. Avoid camelCase, snake_case or PascalCase for classes
6. Avoid the usage of _id_ selector: `#id { ... }`


## Organization

### Properties
To avoid messy CSS code, we like to organize the properties following those steps:

1. *Positioning*: the element's position (position, x/y axis coords, z-index)
2. *Box Model:* the element's behavior (display, margin, padding)
3. *Typography:* the element's text (fonts, colors, text style)
4. *Visual:* the element's appearance (backgrounds, borders, shadows, opacity, outlines)
5. *Misc:* the element's miscellaneous props (perspective, translates, transitions, animations)

### Media queries
Place media queries as near to their relevant blocks as possible. Avoid placing them on a single file or at the end of the document.


## Examples

##### - Properties declaration order:
```css
/* good */
.foo {
  display: block;
  font-size: 1rem;
}

/* bad */
.foo {
  font-size: 1rem;
  position: absolute;
}
```

##### - Declarations per line:
```css
/* good */
.foo {
  display: block;
  font-size: 1rem;
}

.foo,
.bar {
  display: block;
  font-size: 1rem;
}

/* bad */
.foo {
  font-size: 1rem; position: absolute;
}

.bar { font-size: 1rem; }

.foo, .bar { color: red; }
```

##### - Spaces:
```css
/* good */
.foo {
  display: block;
  font-size: 1rem;
}

/* bad */
.foo{
  display:block;
  font-size :1rem;
}

.bar { font-size: 1rem; }
```

#### - Naming
We like very much of [BEM](http://getbem.com/) as a naming pattern:

```css
/* good */
.block {
  display: block;
}

.block__element {
  padding: 2rem;
  color: red;
}

.block__element--modifier {
  color: yellow;
}

/* bad */
.block__element__element {
  ...
}
```


## Tools and methodologies
We like to use those tools and methodologies when coding CSS:

#### Pre/Post Processors
- [Sass](https://sass-lang.com/)
- [PostCSS](https://postcss.org/)

#### Linters
- [Stylelint](https://stylelint.io/)

#### Methodologies (naming, structure)
- [BEM](http://getbem.com/)
- [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/)
- [rscss](https://rscss.io/)


## CSS-in-JS
We also use CSS-in-JS in some projects. The same style is applied then - for declarations, properties, media queries...

A special usage case for CSS-in-JS tools is to develop "white labeled" projects, due to its conditional CSS render.

If possible, prefer to use plain CSS over CSS-in-JS.


## See also
If it would help, take a look at those cool references:

- [Code Guide by @mdo - CSS](https://codeguide.co/#css)
