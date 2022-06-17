## Layouts

- **CSS Box Model**



- **Size elements**

  - width/height
  - padding
  - border
  - margin 



- **Overflowing**

  ```css
  '''X Y'''
  '''visible hidden auto'''
  .box{
  	overflow: auto auto
  }
  ''' overflow 定义当一个元素的内容太大而无法适应 块级格式化上下文 时候该做什么。'''
  ''' 它是 overflow-x 和overflow-y的 简写属性。'''
  ```



- **Measurement Units**

  - Absolute: 

    ```css
    px
    ```

  - Relative: 

    ```css
    %, vm, vh, em, rem
    ```



- **Positioning**

  ```css
  body {
    height: 200vh;
  }
  .boxes {
    position: relative;
    border: 3px solid gray;
  }
  .box {
    width: 5rem;
    height: 5rem;
  }
  .box-one {
    /* independent, ignored by parent element */
    position: absolute;
    background: gold;
  }
  .box-two {
    background: tomato;
    position: relative;
    left: 3rem;
    bottom: -3rem;
    z-index: 1;
  }
  .box-three {
    /* independent, ignored by parent element */
    position: fixed;
    width: auto;
    left: 10rem;
    right: 10rem;
    top: 10px;
    background: dodgerblue;
  }
  ```

  ```html
  <body>
    <div class='boxes'>
      <div class='box box-one'></div>
      <div class='box box-two'></div>
      <div class='box box-three'></div>
    </div>
  </body>
  ```

  - Relative: relative to the its normal position
  - Absolute: relative to the parent
  - Fixed: relative to the viewport



- **Floating elements**

  ```css
  .tweet{
    border: 3px solid gray
  }
  .clearfix::after{
    content: "";
    display: block;
    clear: both;
  }
  .avatar{
    width: 5rem;
    height: 5rem;
    background-color: gold;
    float: left;
    margin-right: 0.5rem
  }
  .content{
    clear: left/right/both
  }
  ```

  ```html
  <html>
  	<body>
      <article class="tweet clearfix">
  			<div class="avatar"></div>
        <p>Lorem ipsum dolor sit amet.</p>
        <p class="content">Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit 					amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet.
        </p>
      </article>
    </body>
  </html>
  ```



- **FlexBox & Grid layouts**

  - **Flex**

    - **display**: flex

    - Axes: 

      - Main (Primary), 
      - Cross (Secondary)
      - **flex-direction**

    - Align Items: 

      - **justify-content** (along the main axis)
      - **align-items** (along the cross axis)
      - **align-content**

      ```css
      .container {
        border: 3px solid lightgray;
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;
        /* flex-wrap: wrap; */
        /* align-content: center; */
        height: 90vh;
      }
      .box {
        width: 5rem;
        height: 5rem;
        background: gold;
        margin: 1rem;
      }
      .box-one {
        align-self: flex-start;
      ```

    - Sizing Items:

      - **flex-basis** (the initial size of a flex item)
      - **flex-grow** (the growth factor)
      - **flex-shrink** (the shrink factor)
      - **flex** (short-hand property)

      ```css
      .box {
        /* flex-basis: 15rem; */
        flex-grow: 1;
        flex-shrink: 2;
        /* flex: 1 1 15rem; */
        width: 5rem;
        height: 5rem;
        background: gold;
        margin: 1rem;
      }
      .box-one {
        flex-grow: 2;
        flex-shrink: 0;
        align-self: flex-start;
      }
      ```

      ```html
      <html>
      	<body>
          <div class="container">
            <div class="box box-one">A</div>
            <div class="box">B</div>
            <div class="box">C</div>
            <div class="box">D</div>
            <div class="box">E</div>
            <div class="box">F</div>
          </div>
        </body>
      </html>
      ```

  - **Grid**

    - Define a grid
      - **display**: grid
      - **grid-template-rows**
      - **grid-template-columns**
      - **grid-template**
    - Align Items
      - **justify-items** (along the horizontal axis)
      - **align-items** (along the vertical axis)
    - **Gap**
      - row-gap
      - column-gap
      - gap
    - **Placing Items**
      - grid-row
      - grid-column
      - grid-area

    ```css
    .container {
      display: grid; /* 3x2 */
      /* grid-template-rows: repeat(3, 100px);
        grid-template-columns: repeat(2, 100px); */
      grid-template: 100px auto 100px/ 30fr 70fr;
      grid-template-areas:
        "header header"
        "sidebar main"
        ". footer";
      /* justify-items: center; */
      /* align-items: center; */
      /* justify-content: center; */
      /* align-content: center;  */
      /* row-gap: 10px; */
      /* column-gap: 10px; */
      gap: 10px 10px;
      height: 90vh;
      border: 3px solid gray;
    }
    .box {
      /* width: 5rem;
        height: 5rem; */
      background: gold;
    }
    .box-one {
      /* grid-column: 1 / 3;
        grid-row: 2 / 5; */
      /* start / end */
      /* row / column */
      /* grid-area: 1 / 1 / 1 / 3; */
      grid-area: header;
    }
    .box-four {
      grid-area: footer;
    }
    ```

    ```html
    <body>
      <div class="container">
        <div class="box box-one">A</div>
        <div class="box">B</div>
        <div class="box">C</div>
        <div class="box box-four">D</div>
      </div>
    </body>
    ```

  - **Hide Elements**

    - display: none
    - visibility: hidden



- **Media Queries**	

```css
.container {
  display: flex;
  flex-direction: row;
}
.box {
  background: gold;
  padding: 1rem;
}
.box:nth-child(2n) {
  background: dodgerblue;
}
@media screen and (max-width: 600px) {
  .container {
    flex-direction: column;
  }
}
```

```html
<div class="container">
  <div class="box">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore
      pariatur dolore voluptates cumque temporibus. Libero corporis
      distinctio dolorem accusamus, iusto quasi voluptatem maiores amet
      mollitia quidem similique perferendis enim ratione, beatae nesciunt
      blanditiis asperiores, sint repudiandae sed. Quo molestias iusto
      perferendis pariatur fuga hic ut, neque suscipit iste, quos mollitia?
    </p>
  </div>
  <div class="box">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas odit
      quas eius quo non et magni vero alias debitis dicta neque ipsa fuga
      numquam excepturi repudiandae aut nesciunt cum provident illum maiores
      a, molestias tempore quis. Earum numquam, voluptatem commodi quam
      deserunt molestias harum expedita obcaecati, est pariatur assumenda
      aliquid.
    </p>
  </div>
</div>
```

