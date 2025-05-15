# HTML Form

`<form>` element is a great tool for collecting information, but then we need to send that information somewhere else for processing. We need to supply the `<form>` element with both **location of where the `<form>`'s information goes** and **what HTTP request to make**.

```
<form action="/example.html" method="POST">
</form>
```
In the example above, `<form>` will send information to **example.html** as a POST request:
- `action` : determines where the information is sent
- `method` : assigned a HTTP verb that is included in HTTP request

`POST` is one of the HTTP requests used by browser and clients to send data to a server. The data is sent in the request body not the URL.
`/example.html` refers to the root of the website

```
<form action="location" method="POST">
    <h1>Creating a form</h1>
    <p>Some contents</p>
</form>
```

## Input
### text
`<input>` element allows user to type their input. It has a `type` attribute which determines how it renders on the web page and what kind of data it can accept. Default value of `type` is `text`. It is also important that we include `name` attribute in the `<input>`,otherwise the information won't send when the `<form>` is submitted.
```
<form action="/example.html" method="POST">
    <input type="text" name="first-text-field">
</form>
```
In the example above, a empty box will form.

<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 173457.png"/>

After user types into the `<input>` element, the value of the `value` attribute becomes what is typed into the text field. The value of `value` attribute is paired with the value of the `name` attribute and send as text when the form is submitted.
For instance, if the user types "abc". When the form is submitted, the text: `"first-text-field=important details"` is send to `/example.html`.

We could also assign a default value for the `value` attribute so that users have a pre-filled text field when they first see the rendered form.
```
<form action="/example.html" method="POST">
    <input type="text" name="first-text-field" value="already pre-filled">
</form>
```

### password
`<input type="password">` element will replace input text with another character (* / •)
```
<form>
    <label for="user-password">Password:</label>
    <input type="password" id="user-password" name="user-password">
</form>
```
It would look like this : 
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 175954.png">

### number
By setting `type="number"` , we can restrict what users type into the input field to just numbers( and a few special characters like `-`,`+` and `.`). We can also provide a `step` attribute which creates arrows inside the input field to increase / decrease by the value of the `step` attribute.
```
<form>
    <label for-"years">Years of experience:</label>
    <input id="years" name="years" type="number" step="1">
</form>
```
It would look like this: 
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 182332.png">

### range
`range` is similar like `number` but it is able to limit what numbers our users could type. To set the min and max value, we use `min` and `max` attributes of the `<input>`
```
<form>
    <label for="volume">Volume Control</label>
    <input id="volume" name-"volume" type="range" min="0" max="100" step="1">
</form>
```
It would look like this:
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 183004.png">

### checkbox
We can present multiple options to user by setting `type="checkbox"`
```
<form>
  <p>Choose your pizza toppings:</p>
  <label for="cheese">Extra cheese</label>
  <input id="cheese" name="topping" type="checkbox" value="cheese">
  <br>
  <label for="pepperoni">Pepperoni</label>
  <input id="pepperoni" name="topping" type="checkbox" value="pepperoni">
  <br>
  <label for="anchovy">Anchovy</label>
  <input id="anchovy" name="topping" type="checkbox" value="anchovy">
</form>
```
It would look like this:
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 183628.png">

In the example above, there are assigned values to the `value` attribute of the checkboxes. These values are not visible on the form itself.

### radio button
Radio button input allows user to choose only one choice.
```
<form>
    <p>What is sum of 1+1?</p>
    <input type="radio" id="two" name="ans" value="2">
    <label for="two">2</label>
    <br>
    <input type="radio" id="eleven" name="ans" value="11">
    <label for="eleven">11</label>
</form>
```
It would look like this:
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 185535.png">

### dropdown list
Dropdown list allow users to choose one option from an organized list.
```
<form>
    <label for="lunch">What's for the lunch?</label>
    <select id="lunch" name="lunch">
        <option value="pizza">Pizza</option>
        <option value="curry">Curry</option>
        <option value="salad">Salad</option>
        <option value="ramen">Ramen</option>
    </select>
</form>
```
It would look like this:
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 190046.png">

### datalist
Even if we have an organized dropdown list, if the list has a lot of options, it could be tedious for users to scroll through the entire list to locate one option. `<datalist>` is used with an `<input type="text">` element. The input creates a text field that users can type into and filter option from the `<datalist>`.
```
<form>
    <label for="city">Ideal city to visit?</label>
    <input type="text" list="cities" id="city" name="city">

    <datalist id="cities">
        <option value="New York City"></option>
        <option value="Tokyo"></option>
        <option value="Barcelona"></option>
        <option value="Mexico City"></option>
        <option value="Melbourne"></option>
    </datalist>
</form>
```
It would look like this:
<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-14 190909.png">

### textarea
`<textarea>` element is used to create a bigger text field for users to write more text. We can add the attributes `rows` and `cols` to determine the amount of rows and columns for the `<textarea>`.
```
<form>
    <label for="blog">New Blog Post:</label>
    <br>
    <textarea id="blog" name="blog" rows="5" cols="30">
    </textarea>
</form>
```

## Label
The `<label>` element has an opening and closing tag and displays text that is written between the opening and closing tags. To associate a `<label>` and an `<input>`, the `<input>` needs an `id` attribue.
```
<form action="/example.html" method="POST">
    <label for="meal">What do you want to eat?</label>
    <br>
    <input type="text" name="food" id="meal">
</form>
```
When `<label>` element is clicked, the corresponding `<input>` is highlighted.