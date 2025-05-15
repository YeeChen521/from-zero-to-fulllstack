# Semantic HHTML
When building web pages, we use a combinattion of non-semantic HTML and Semantic HTML. By using Semantic HTML, we select HTML elements based on their meaning, not on how they are presented. Elements such as `<div>` and `<span>` are not semantic elements since they provide no context as to what is inside of those tags.

For example, instead of using a `<div>` element to contain our header information, we could use a `<header>` element which is used as a headings section.

**Why use Semantic HTML?**
- **accessibility** : makes webpages accessible for mobile devices and for people with disabilities as well.
- **SEO** : improve the websice SEO which is the process of increasing the number of people that visit your webpage.
- **easy to understand** : makes the website's source  code easier to read for other web developers.

<img src="C:\Users\USER\OneDrive\Pictures\Screenshots\Screenshot 2025-05-15 172721.png">

## Header and Nav
`<header>` is a container usually for either navigational links or introductory content containing `<h1>` to `<h6>` headings.
```
<header>
    <h1> Everything you need to know about pizza! </h1>
</header>
```

`<nav>` is used to define a block of navigation links such as menus and tables of contents. It is important to note that `<nav>` can be used inside of the `<header>` element but can also be used on its own.
```
<header> 
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>   
    </ul>
  </nav>
</header>
```

## Main and Footer
The element `<main>` is used to encapsulate the dominant content within a webpage. This tag is separate from the `<footer>` and the `<nav>` of a web page since these elements don't contain the principal content.
```
<main>
    <header>
        <h1>Types of Sports</h1>
    </header>
    <article>
        <h3>Baseball</h3>
        <p>The first game of baseball was played in Cooperation, New York in the summer of 1839.</p>
    </article>
</main>
```
The content at the bottom of the subject information is known as *footer*, indicated by the `<footer>` element. The footer contains information such as:
- contact information
- copyright information
- terms of use
- site map
- reference to top of page links
```
<footer>
    <p>Contact number : +60-12 3456789</p>
</footer>
```

## Article and Section
`<section>` defines elements in a document such as chapters, headings or any other area of the document with the same theme. A website's homepage could be split into sections for the introduction, news items and contact information.

`<article>` element holds content that makes sense on its own. `<article>` can hold content such as articles, blogs, comments, magazines, etc.
```
<section>
    <h2>Fun Facts About Cricket</h2>
    <article>
        <p>A single match of cricket can last up to 5 days.</p>
    </article>
</section>
```

## Aside element
`<aside>` element is used to mark additional information that can enhance another element but isn't required in order to understand the main content. Some common uses of the `<aside>` element are for:
- Bibliographies
- Endnotes
- Comments
- Pull quotes
- Editorial sidebars
- Additional information
```
<article>
    <p>The first World Series was played between Pittsburgh and Boston in 1903 and was s nine-game series.</p>
</article>
<aside>
    <p>Babe Ruth once stated,"Heroes get remembered, but legends never die."</p>
</aside>
```

## Figure and Figcaption
`<figure>` is an element used to encapsulate media such as image, illustration, diagram, code snippet, etc, which is referenced in the main flow of the document.
```
<figure>
    <img src="abc.jpg">
</figure>
```
`<figcation>` is an element used to describe the media in the `<figure>` tag.
```
<figure>
    <img src="abc.jpg">
    <figcaption>This picture shows characters from Overwatch.</figcaption>
</figure>
```
While the content in `<figure>` is related to the main flow of the document, its position is independent. This means that you can remove it or move it somewhere else without affecting the flow of document.

## Audio and Attributes
`<audio>` element is used to embed audio content into a document.
```
<audio autoplay controls>
    <source src="address" type="audio/mp3">
</audio>
```
Although `type` is not always necessary, it's recommended that we state the type of audio as it help the browser identify it more easily and determine if the type of audio file is supported by the browser.

## Video and Embed
By using a `<video>` element, we can add videos to our website. Some attributes that can alter a video playblack include:
- `controls`
- `autoplay`
- `loop`

```
<video src="coding.mp4" controls>Video not supported</video>
```
The "Video not supported" will only show up if the browser is unable to display the video.

`<embed>` can embed any media content including videos, audio files and gifs from an external source. This means that websites that have an embed button have some form of media content that can be addded to other websites.

```
<embed src="download.gif"/>
```