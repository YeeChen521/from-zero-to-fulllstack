# Selector
With a selector, we can decide which elements will get the style. A selector is used to target the specific HTML element to be styled by the declaration.

## Type
The type selector matches the *type* of the element in the HTML document.
```
p{
    color:green;
}
```
The type selector does not include the angle brackets. Since element types are often referred to by their tag name, the type selector is sometimes referred to as the *tag name* or *element selector*.

## Universal
*universal* selector selects all elements of any type. Targeting all of the elements on the page has a few specific use cases, such as resettting default browser styling or selecting all children of a parent element. The universal selector uses the `*` character in the same place where you specified the type selector in a ruleset.
```
*{
    font-family:Verdana;
}
```

## Class
CSS is not limited to selecting elements by their type. When working with HTML and CSS a class attribute is one of the most common ways to select an element.
`<p class="brand">Soko Show Company</p>`

In the example above, the `class` attribute is set to `brand`. To select this element using CSS, we can create a ruleset with a class selector of `.brand`.

```
.brand{

}
```

## Multiple Classes
We are able to add more than one class name to an HTML element's `class` attribute.
```
.green{
    color:green;
}
.bold{
    font-weight:bold;
}
```

`<h1 class="green bold">abc</h1>`

We can add multiple classes to an HTML element's `class` attribute by separating them with a space. This enable us to mix and match CSS classes to create many unique styles without writing custom class for every style combination needed.

## Id
If an HTML element needs to be styled uniquely, we can give it an ID using the `id` attribute.
`<h1 id="large-title">abc</h1>`

In contrast to `class` which accept multiple values and can be used broadly throughout an HTML document, an element's `id` can only have a single value and only be used once per page.

To select an element's id with CSS, we prepend the `id` name with a number sign (`#`)
```
#large-title{

}
```

## Attribute
The attribute selector can be used to target HTML element that already contain attributes. Elements of the same type can be targeted differently by their attribute or attribute value.
```
[href]{
    color:magenta;
}
```
In the example above, `[href]` would target all elements with an `href` attribute and set `color` to `magenta`.

By adding type / attribute values, it can get more granular. One way is by using `type[attribute*=value]`

```
<img src='/images/seasons/cold/winter.jpg'>
<img src='/images/seasons/warm/summer.jpg'>
```
```
img[src*='winter'] {
  height: 50px;
}

img[src*='summer'] {
  height: 100px;
}
```
The first ruleset looks for an `img` element with an attribute `src` that contains the string `'winter'` and set the `height` to `50px`.
The second ruleset looks for an `img` element with an attribute of `src` that contains the string `'summer'` and sets the height to `100px`.

## Pseudo-class
You may have observed how the appearance of certain elements can change, or be in a different state after certain user interaction. For instance, when you click on an `input` element and a blue border is added showing it is in focus.

This is an examples of pseudo-class selectors in action. In fact, `:focus`,`:visited`,`:disable` and `:active` are all pseudo-classes.

A pseudo-class can be attached to any selector. It is always written as a colon followed by a name.
```
p:hover{
    background-color:lime;
}
```
In the example above, whenever the mouse hovers over a paragraph element, that paragraph will have a lime-coloured background.

## Specificity
Specificity is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity so that if an element needs a new style, it is easy to override.

Id is the most specific selector in CSS followed by classes and type.

## Chaining
When writting CSS rules, it is possible to require an HTML element to have two or more CSS selectors at the same time. This is done by combining multiple selectors which we will refer as chaining. For instance, if there was a `special` class for `<h1>` elements, the CSS would look like below:
```
h1.special{

}
```
The code above would select only the `<h1>` elements with a class of `special`/ If there is a `<p>` element with class `special`, the rule in the example would not style the paragraph.

## Descendant Combinator
CSS also supports selecting elements that are nested within other HTML elements.
For example, the nested `<li>` elements are descendants of the `<ul>` element and can be selected with the descendant combinator like so:
```
.main-list li{

}
```
`main-list` is the class name for the `<ul>` element.

## Chaining and Specificity
```
p {
  color: blue;
}

.main p {
  color: red;
}

```
In the example above, only the `<p>` element inside the `.main` element will appear `red`. 

## Multiple Selectors
In order to make CSS more concise, it is possible to add CSS styles to multiple CSS selectors all at once. This prevents writing repetitive code.
```
h1 {
  font-family: Georgia;
}

.menu {
  font-family: Georgia;
}
```
In the example above, the code has repetitive style attribute. Instead of writing `font-family:Georgia` twice for two selectors, we can separate the selectors by a comma to apply the same style to both.
```
h1,
.menu{
    font-family:Georgia;
}
```