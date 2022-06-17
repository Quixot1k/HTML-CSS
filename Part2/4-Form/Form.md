## Form



#### Styling Form

```css
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", 	Roboto, Oxygen, Ubuntu, 	Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  line-height: 1.5;
  padding: 1rem;
}
label {
  display: block;
}
input[type="text"],
input[type="email"] {
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 0.3rem 0.5rem;
  transition: border-color 0.15s, box-shadow 0.3s;
}
input[type="text"]:focus,
input[type="email"]:focus {
  border-color: #7db0fb;
  box-shadow: 0 0 0 2px rgba(24, 117, 255, 0.25);
  outline: 0;
}
button {
  background-color: #0d6efd;
  color: #fff;
  border: 0;
  padding: 0.3rem;
  border-radius: 5px;
  outline: 0;
}
.form-group {
  margin-bottom: 1rem;
}
```



#### CSS Framework

- Bootstrap

  ```html
  <form class="w-50" action="">
    <div class="mb-3">
      <label class="form-label" for="name">Name</label>
      <input class="form-control" id="name" type="text" />
    </div>
    <div class="mb-3">
      <label class="form-label" for="email">Email</label>
      <input class="form-control" id="email" type="email" />
    </div>
    <button class="btn btn-primary" type="submit">Register</button>
    <button class="btn btn-secondary" type="reset">Reset</button>
  </form>
  ```

- Milligram



#### Input Area

```html
<form action="">
  <input type="email" placeholder="Email" autofocus />
  <input type="number" />
  <input type="password" maxlength="16" />
  <input type="date" />
  <textarea>Comment...</textarea>
</form>
```



#### DataList

```html
<form action="">
  <input type="text" list="countries" autocomplete="off" />
  <datalist id="countries">
    <option data-value="0">Australia</option>
    <option data-value="1">Canada</option>
    <option data-value="2">US</option>
    <option data-value="3">China</option>
    <option data-value="4">India</option>
  </datalist>
</form>
```



#### Dropdown List

```html
<form action="">
  <!-- <select name="" id="" multiple> -->
  <select name="" id="">
    <optgroup label="Front-end Courses">
      <option value="0" selected>HTML</option>
      <option value="1">CSS</option>
      <option value="2">Javascript</option>
    </optgroup>
    <optgroup label="Back-end Courses">
      <option value="3">Node</option>
      <option value="4">ASP</option>
      <option value="5">Django</option>
    </optgroup>
  </select>
</form>
```



#### CheckBox

```html
<form action="">
  <div>
    <input type="checkbox" name="" id="front-end" checked />
    <label class="label-inline" for="front-end">Front-end</label>
  </div>
  <div>
    <input type="checkbox" name="" id="back-end" />
    <label class="label-inline" for="back-end">Back-end</label>
  </div>
</form>
```



#### Radio Button

```html
<form action="">
  <div>
    <input type="radio" name="menbership" id="gold" />
    <label for="" class="label-inline">Gold</label>
  </div>
  <div>
    <input type="radio" name="menbership" id="silver" />
    <label for="" class="label-inline">Silver</label>
  </div>
</form>
```



#### Slider & Files

```html
<form action="">
  <input type="range" name="" id="" min="0" max="100" value="75" />
  <input type="file" name="" id="" multiple accept=".pdf, .doc, .docx" />
</form>
```



#### Grouping Related Fields

```html
<form action="">
  <fieldset>
    <legend>Billing Address</legend>
    <input type="text" />
    <input type="text" />
    <input type="text" />
  </fieldset>
  <fieldset>
    <legend>Payment</legend>
    <input type="hidden" name="course-id" value="123" />
    <input type="text" />
    <input type="text" />
    <input type="text" />
  </fieldset>
</form>
```



#### Submitting

```html
<!-- formspree -->
<form action="https://formspree.io/f/mlezjzlz" method="post">
  <input type="text" placeholder="Name" name="name" required />
  <input type="text" placeholder="Email" name="email" required />
  <button type="submit">Submit</button>
</form>
```

