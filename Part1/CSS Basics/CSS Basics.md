## CSS Basics

##### Ways to provide CSS

- Embedded stylesheets

- External stylesheets 

  ```css
  <link rel="stylesheet" href="styles.css">
  ```

- Inline styles

---

##### Normalizing

  ```css
  <link rel="stylesheet" href="normalize.css">
  ```

---

##### Selectors

- Basic Selcetors

  ```css
  a[href="www.google.com"]{
    color: "#ccc"
  }
  a[href*="google"]{
    color: "#ccc"
  }
  a[href^="www"]{
    color: "#ccc"
  }
  a[href$="com"]{
    color: "#ccc"
  }
  <a href="www.google.com" target="_blank"></a>
  ```

- Relational Selectors

  ```css
  '''descendent selector'''
  #products p{
    color: "#ccc"
  }
  '''direct-child selector'''
  #products > p{
    color: "#ccc"
  }
  '''direct-sibling selector'''
  #products + p{
    color: "#ccc"
  }
  '''general-sibling selector'''
  #products ~ p{
    color: "#ccc"
  }
  ```

  ```html
  <html>
    <body>
      <section id="products">
        <p>Lorem ipsum dolor sit amet.</p>
        <article>
          	<p>Lorem ipsum dolor sit amet.</p>
        </article>
      </section>
      <p>Lorem ipsum dolor sit amet.</p>
      <p>Lorem ipsum dolor sit amet.</p>
    </body>
  </html>
  ```

- Pseudo-class Selector

  ```css
  article:first-child{
    color: "#ccc"
  }
  article:last-child{
    color: "#ccc"
  }
  article:first-of-type{
    color: "#ccc"
  }
  article:last-of-type{
    color: "#ccc"
  }
  ```
  
  ```css
  ul li:nth-child(odd/even){
    color: "#ccc"
  }
  ul li:nth-child(3n){
    color: "#ccc"
  }
  ```
  
  ```css
   a:link{
    color: "#ccc"
  }
  a:visited{
    color: "#ccc"
  }
  a:hover a:focus{
    color: "#ccc"
  }
  ```
  
  ```html
  <html>
    <body>
      <article>
        <a href="https://"></a>
        <p>Lorem ipsum dolor sit amet.</p>
        <p>Lorem ipsum dolor sit amet.</p>
      </article>
    </body>
  </html>
  ```
  
- Pseudo-elements Selector

	```css
	p::first-letter{
	  font-size: 140%
	}
	p::first-line{
	  font-weight: "bold" 
	}
	p::selection{
	  color: "pink"
	}
	p::before{
	  content: "...";
	  display: block;
	}
	p::after{
	  content: "...";
	  display: inline;
	}
	```

---

##### Colors

- Named colors

- RGB
- HSL
- Hex

---

##### Gradients

- Linear-gradient

  ```css
  .box{
    background: linear-gradient(45deg, blue, yellow, red)
  }
  ```

- Radial-gradient	

  ```css
  .box{
    background: radial-gradient(45deg, blue, yellow, red)
  }
  ```

---

##### Borders

```css
.box{
	border: 10px solid blue
}
.box{
	border: 10px dashed blue
}
.box{
	border-top: 10px solid blue
}s
.box{
	border-width: 10px 20px 30px 40px	'''top right bottom left'''
}
.box{
	border-radius: 50px
}
```

---

##### Shadows

```css
'''horizontal	vertical	blur	color'''
.box{
	box-shadow: 10px 10px 30px grey
}
h1{
	text-shadow: 10px 10px 30px rgba(0,0,0,0.2)
}
```

