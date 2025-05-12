# HTML Document Standards
An HTML document is a file that uses HTML to structure content for the web. It tells a web browser how to display text, imgae, links, video and other elements on a webpage.

We need a cdocument type declaration to let the web browser know that we are using HTML by starting our document. This declaration is an instruction and it must be the **first line of the code**.** It tells web browser what **version of HTML** is being used in the document and the **type of document**. Currently, `<!DOCTYPE html>` is referring to HTML5.

`<!DOCTYPE html>`

Don't forget to save your HTML file with an **.html** extension.

To create HTML structure and content, we must add opening and closing `<html>` tags after declaring `<!DOCTYPE html>`.

```
<!DOCTYPE html>
<html>

</html>
```

## Head
`<head>` element is part of the HTML methaphor. It goes above the `<body>` element. It contains the metadata (information about the page that isn't displayed directly on the web page) for a web page.

### page title
A browser's tab displays the title specified in the `<title>` tag. The `<title>` tag is always inside of the `<head>`.

`<title></title>`

## Internal Web Pages
Internal web pages are within the same website or domain such as Home, Contacts and About.

## External Web Pages
External Web Pages are on a different web sites or domain.

## Link to Relative Page
Before learning how to link between internal pages, we must establish where our files are stored. When making multipage static websites, web developers often store HTML files in the root directory or a main folder where all the files for the project are stored.
```
project-folders/
|—— about.thml
|—— contact.html
|—— index.html
```

If the browser currently displaying index.html, it also knows the about.html and contact.html are in the same folder because the files are stores in the same folder. Therefore, we are able to link web pages together using a relative path.

`<a href="./contact.html">Contact</a>`

`./` tells the browser to look for the file in the current folder

## Link at Will
Turn images into links by simply wrapping the `<img>` element with an `<a>`

`<a href="link location" target="_blank"><img src="image location" alt="xyz"/></a>`

## Link to Same Page
When a page has too much content, it makes the user hard to jump to different positions of our pages. When users visit our site, we want them to be able to **click a link** and have the page **automatically scroll to a specific section**. Therefore, we must give the target an `id` attribute and a unique value.
```
<p id="top">This is the top of the page!</p>
<h1 id="bottom">This is the bottom!</h1>
```
A `id` should be descriptive to make it easier to remember the purpose of a link. The target link is a string containing the `#` character and the target element;s `id`/

```
<ol> 
    <li><a href="#top">Top</a></li>
    <li><a href="#bottom">Bottom</a></li>
</ol>
```
