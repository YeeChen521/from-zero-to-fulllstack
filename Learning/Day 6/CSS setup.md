# Intro to CSS

CSS is a language web developers use to style the HTML content on a web page.

## CSS Anatomy
![CSS syntax](../../Image/Screenshot%202025-05-16%20164554.png)
The first syntax shows CSS applied as a ruleset while the second shows it written as inline style. Both syntax contain a declaration. Declarations are the core of CSS. They apply a style to the selected element. Here, the `<p>` element has been selected in both syntaxes and will be styled to display the text in blue.
**Ruleset Terms** :
- *selector* : the beginning of the ruleset used to target the element that will be styled.
- *declaration block* : the code in between the curly braces that contains the CSS declaration
- *declaration* : the group name for a property and value pair that applies a style to the selected element
- *property* : the first part of the declaration that signifies what visual characteristic of the element is to be modified
- *value* : the second part of the declaration that signifies the value of the property

**Inline Style Terms** :
- *opening tag* : the start of an HTML element 
- *attribute* : the style attribute is used to add CSS inline styles to an HTML element

## Internal Stylesheet
Inline styles are not best way to style HTML elements. For example, multiple `<h1>` elements you would have to add inline styling to each manually.

Fortunately, HTML allows you to write CSS code in its own dedicated secton with a `<style>` element nested inside of the `<head>` element. 
```
<head>
    <style>
        p{
            color: red;
            font-size: 20px;
        }
    </style>
</head>
```
The CSS code in the example above changes the color of all paragraph text to read and also changes the size of the text to 20 pixels.

## External Stylesheet
To avoid mixing code, we separate the HTML and CSS code in separate file. However, we must link the CSS file to HTML file.

`<link>` element must be placed within the head of the HTML file. It is a self-closing tag and requires the following attributes:
- `href` : the value of this attribute must be the address to the CSS file
- `rel` : this attribute describes the relationship between the HTML and CSS file

```
<link href="css file location" rel="stylesheet">
```

