## Typography



#### Styling fonts

```css
body {
  margin: 10px;
  font-family: Arial, Helvetica, sans-serif;
}
h1 {
  font-family: Georgia, "Times New Roman", Times, serif;
}
p {
  font-weight: normal;
  font-style: italic;
  font-size: 1rem;
  color: #222;
}
```



#### Embedding custom fonts

```css
@font-face {
  font-family: "opensans";
  src: url("fonts/open-sans/opensans-bold-webfont.woff2") format("woff2");
  font-weight: bold;
  font-style: normal;
}

@font-face {
  font-family: "opensans";
  src: url("fonts/open-sans/opensans-regular-webfont.woff2")
    format("woff2");
  font-weight: normal;
  font-style: normal;
}
```

- Flash of Undstyled Text		

```css
body {
  margin: 10px;
  font-family: "opensans", Arial, Helvetica, sans-serif;
  font-display: optional;
}
```



#### System Font Stack

```css
h1 {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
```



#### Best practices for text size & spacing

- Vertical Spacing

  - marigin
  - line-height

- Horizontal Spacing

  - letter-spacing
  - word-spacing

  

#### Formatting text

- text-align

- text-indent

- text-decoration

- text-transform

- white-space

- text-overflow

- column-*

  ```css
  p {
    width: 60ch;
    font-weight: normal;
    font-style: italic;
    color: #222;
    column-count: 2;
    column-gap: 2rem;
    column-rule: 3px groove #fff;
  }
  ```

- direction

