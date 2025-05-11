# Intro to HTML (HyperText Markup Language)

- Provides structure to the content appearing on a website

*markup* language is a computer language that defines the structure and presentation of raw text. In HTML, the computer can interpret raw text thats is wrapped in the HTML **elements**.
HyperText us text displayed on a computer device that provides access to other text through **links** (hyperlinks).

## HTML Structure
HTML is organised as a **collection of family tree relationships**. When an element is contained inside another element, it is considered the child of that element. The child element is said to be nested inside of the parent element.

```
<body>
    <div>
        <h1>Sibling to p, but also grandchild of body</h1>
        <p>Sibling to h1, but also grandchild of body</p>
    </div>
</body>
```
In the example aboe, `<body>` element is the parent for `<div>` and the grandparent for `<h1>` and `<p>`. `<div>` is the parent for `<h1>` and `<p>`.

## Element
Element contains :
- tag : the element name surrounded by an opening(`<`) and closing (`>`) angle bracket
- opening tag : the first HTML tag used to start an HTML element
- content : the information contained between the opening and closing tags of an HTML element
- closing tag : the second HTML tag used to end an HTML element

### header 
`<h1>` is used for the main header. It is used for the most important headings on the webpage and browsers typically render it as large, bold text.

There are six different headings, from h1 to h6.

```html
<h1>chewyeechen</h1>
```

### paragraph
It contains a block of plain text
`<p>What's up, doc?</p>`

### span
It contains short pieces of text or other HTML. It is used to **seperate small pieces of content** that are on the **same line** as other content.

```
<div>
    <p><span>Self-driving cars</span> are anticipated to replace up to 2 milion jobs over the next two decades.</p>
</div>
```

### body
**Everything inside the body will be displayed on the screen.** Different types of content (text,images and buttons) can be added to the body

```
<body> 
    <p>  </p>
</body>
```

### division
It used for **grouping content without implying any specific meaning**. It also common use for CSS for layout and styling.

It does not inherently have a visual representation.
`<div> </div>`

### line breaks
It is only composed of a starting tag.

```
<p>The Nile River is the longest river <br> in the world, measuring over 6,850 <br> kilometers long (approximately 4,260 <br> miles).</p>
<!-- The Nile River is the longest river
in the world, measuring over 6,850
kilometers long (approximately 4,260
miles). -->
```

### unordered list
`<ul>` is used to create a list of items in no particular order. It should not hold raw text and wont automatically foramt raw text into an unordered list of items. Therefore, `<li>` must be added to the raw test.

```
<ul>
    <li>Limes</li>
    <li>Tortillas</li>
    <li>Chicken</li>
</ul>
```
### ordered list
Each list item is **numbered**.
```
<ol>
    <li>Preheat the oven to 350 degrees.</li>
    <li>Mix whole wheat flour, baking soda and salt.</li>
    <li>Cream the butter,sugar in separate bowl.</li>
    <li>Add eggs and vanila extracts to bowl.</li>
</ol>
```

## Attributes
It is used for **expand an element's tag**. Attributes are content added to the opening tag of an element and can be used in several different ways from providing information to change styling. 
Attributes are made up of following two parts :
- The *name* of the attributes
- The *value* of the attributes

```
<div id ="intro">
    <h1> Introduction</h1>
</div>
```
`id` is commonly used for specific different content which is useful when reusing the element.


## Styling Text
- emphasizes text (italic) : `<em>`
- highlights important text (bold) : `<strong>`

```
<p><strong>The Nile River </strong> is the <em> longest</em> river in the world, measuring over 6580 kilometers long (approximately 4260 miles).</p>
<!-- The Nile River is the longest river in the world, measuring over 6580 kilometers long (approximately 4260 miles).-->
```
