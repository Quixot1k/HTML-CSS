## Images



#### Background Images

```css
body {
  background: url(./images/bg-sanfrancisco.jpg);
  background-repeat: no-repeat;
  /* background-position: 100px 100px; */
  background-size: cover;
  background-attachment: fixed;
  height: 300vh;
}
```



#### CSS Sprites

```css
.css-sprite-dishes {
  background: url("./CSS-Sprite-Package/css-sprite-combined.png") 0px -0px;
  width: 100px;
  height: 100px;
  display: inline-block;
}

.css-sprite-landing {
  background: url("./CSS-Sprite-Package/css-sprite-combined.png") -100px -0px;
  width: 100px;
  height: 100px;
  display: inline-block;
}

.css-sprite-rocketship {
  background: url("./CSS-Sprite-Package/css-sprite-combined.png") -200px -0px;
  width: 100px;
  height: 100px;
  display: inline-block;
}

.css-sprite-saturn {
  background: url("./CSS-Sprite-Package/css-sprite-combined.png") -300px -0px;
  width: 100px;
  height: 100px;
  display: inline-block;
}

.css-sprite-ufo {
  background: url("./CSS-Sprite-Package/css-sprite-combined.png") -400px -0px;
  width: 100px;
  height: 100px;
  display: inline-block;
}
```

```html
<span class="css-sprite-dishes"></span>
<span class="css-sprite-landing"></span>
<span class="css-sprite-rocketship"></span>
<span class="css-sprite-saturn"></span>
<span class="css-sprite-ufo"></span>
```

- Problems
  - File size can get too large
  - Sprites are not flexible



#### Data URI

- use data uri generator
- Problems
  - Size gets larger than original resource
  - Increased complexity
  - Slow on mobile



#### Clipping & Filter

Use clip-path maker !!!

```css
.meal {
  clip-path: polygon(75% 0%, 100% 50%, 75% 100%, 0% 100%, 25% 50%, 0% 0%);
  filter: grayscale(40%) blur(2px);
}
```

```html
<img class="meal" src="images/meal.jpg" alt="" />
```



#### High Density Screen

```css
<img
  class="meal"
  src="images/meal.jpg"
  alt=""
  srcset="images/meal.jpg 1x, images/meal@2x.jpg 2x, images/meal@3x.jpg 3x"
/>
```



#### Resolution Switching

```css
<img
  class="meal"
  src="images/meal.jpg"
  alt=""
  srcset="
    images/meal.jpg     400w,
    images/meal@2x.jpg  800w,
    images/meal@3x.jpg 1200w
  "
  sizes="(max-width: 500px) 100vw, 
  (max-width: 700px) 50vw,
  33vw"
/>
```



#### Art Direction

```html
<picture>
  <source media="(max-width: 600px)" srcset="./images/meal-cropped.jpg" />
  <source media="(min-width: 600px)" srcset="./images/meal.jpg" />
  <img src="./images/meal.jpg" alt="" />
</picture>
```

###### 

#### SVG/Icon Fonts

- fontawesome.com

