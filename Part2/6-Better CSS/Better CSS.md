## Better CSS



#### CSS Best Practices

- Follow a naming convention
  - kebab case
  - camel case
  - pascal case
- Create logical sections in your stylesheet
- Avoid over-specific selectors
- Avoid !important
- Sort CSS properties
- Take advantage of style inheritance
- Extract repetitive patterns



#### CSS variables

```css
:root{
  --color-primary:  #ccc;
  --border-size: 2px;
  --border-radius: 10px;
}
.one{
  background: var(--color-primary)
}
.two{
  background: var(--color-primary)
}
```



#### Object-oriented CSS

- Seperate container and content 
- Seperate skin and structure



#### BEM(Block Element Modifier)



