## Transformation, Transition, Animation



#### Transformations

- rotate()
- scale()
- skew()
- translate()

```css
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
.box {
  width: 100px;
  height: 100px;
  background: gold;
  overflow: hidden;
  /* display: inline-block; */
}
.container {
  perspective: 200px; /* 2 boxes share the same perspective */
}
.container:hover .box {
  transform: translateZ(50px) rotateY(45deg);
  transform-origin: 0 50%;
}
.container:hover .box-special {
  transform: rotateX(45deg);
}
```

```html
<body>
  <div class="container">
    <div class="box">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis nostrum,
      fuga eligendi quod nobis enim sint perferendis facere blanditiis
      placeat!
    </div>
    <div class="box box-special">
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis nostrum,
      fuga eligendi quod nobis enim sint perferendis facere blanditiis
      placeat!
    </div>
  </div>
</body>
```



#### Transitions

```css
.box {
  width: 100px;
  height: 100px;
  background: gold;
  overflow: hidden;
  perspective: 200px;
  transition: transform 0.5s, background-color 0.5s;
  /* display: inline-block; */
}
```



#### Animations

```css
@keyframes pop {
  0% {
    transform: scale(1);
  }
  25% {
    transform: scale(1.3);
  }
  50% {
    transform: rotate(360deg);
    background-color: tomato;
  }
  100% {
    transform: rotate(0deg);
  }
}
.box {
  overflow: hidden;
  width: 100px;
  height: 100px;
  background: gold;
  animation-name: pop;
  animation-duration: 3s;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-out;
  animation-direction: alternate;
}
```

- Resuse animations

    ```css
    @keyframes pop {
      0% {
        transform: scale(1);
      }
      25% {
        transform: scale(1.3);
      }
      50% {
        transform: rotate(360deg);
        background-color: tomato;
      }
      100% {
        transform: rotate(0deg);
      }
    }
    .box {
      overflow: hidden;
      width: 100px;
      height: 100px;
      background: gold;
    }
    .animation-pop {
      animation-name: pop;
      animation-duration: 3s;
      animation-delay: 2s;
      animation-iteration-count: infinite;
      animation-timing-function: ease-out;
      animation-direction: alternate;
    }
    ```

      ```html
      <!-- animate.style -->
      <div class="box animation-pop">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Omnis nostrum,
        fuga eligendi quod nobis enim sint perferendis facere blanditiis placeat!
      </div>
      ```

