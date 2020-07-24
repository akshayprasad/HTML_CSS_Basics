HTML and CSS beginners guide
=================

### Basic Introduction

I'm Akshay Prasad. I'm an engineer and a Masters student and I've been working on HTML, CSS, web development and scripting for over 4 years. I would like to share some insights on the same.


## Table of Contents
 * [HTML](https://github.com/akshayprasad/HTML_CSS_Basics#html-time)
	* Editors
	* Tag Structure
	* Text Structure
	* Links
	* Images
	* Line Breaks
	* Tables
	* Colors
	* Width and Height
	* Borders
	* Text Styles

 * [CSS](https://github.com/akshayprasad/HTML_CSS_Basics#some-more-css)
	
	* Classes
	* IDs
	* Other important tags
		* `<span>` tag
		* `<div>` tag
			* Background color
			* Floating
			* Positioning
			* Margins and Padding
			* Z-Index
		* `<link>` Tag, Comments
			* The `<link>` tag
			* Commenting
				* HTML Comments
				* CSS Comments
				* Forms
				* HTML5 and CSS3
 * [Final Overall!](https://github.com/akshayprasad/HTML_CSS_Basics#project)

## HTML Time

### Editors

We need a platform to edit the code that we have. I personally used these editors in my experience

<ul>
	<li><a href="https://code.visualstudio.com">Visual Studio Code</a></li>
	<li><a href="https://atom.io/">Atom</a></li>
	<li><a href="https://www.sublimetext.com/">Sublime</a></li>
	<li><a href="http://notepad-plus-plus.org">Notepad++</a></li>
</ul>

There's a bunch of others [listed here](http://en.wikipedia.org/wiki/List_of_HTML_editors), I just listed the ones I've used and liked!

### Tag Structure

There is a HTML page, about as simple as you can get.  You can open it up in the **Structure** folder in the file page1.html.  If you were to open the file in your favorite browser (which you can do, go ahead), you'll see a plain webpage with the title "Sample page" and the words, "Hello, programmer!" written on the page.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>
      Sample page
    </title>
  </head>
  <body>
    Hello, programmer!
  </body>
</html>
```

Tags organize your page and tell the browser what your page consists of.  There's tons of tags out there, some that you may never use.  
Here's some lists of tags if you really care to see all of them at this point:
 * [W3Schools Tag List](http://www.w3schools.com/tags/default.asp)

So, if you look at our example, you can also put tags inside other tags (like we did with the `<title>` tags inside the `<head>` tags).  This is called *nesting* elements.
In this case, we would say that the `<head>` *contains* the `<title>`.  Sometimes when you have a lot of nested tags, it's hard to keep track, so you have to format your code with spacing, as shown.  Typically, inner tags are spaced more than their outer tags (just as `<title>` is indented further than `<head>`).

Let's take a look again at part1.html in the **Structure** folder.  You'll notice that the first line has `<!doctype html>`.  Every HTML document and website has to have this special tag, as it tells the browser what language we're using.  This is one of those special tags I mentioned that doesn't need a closing tag.

On the second line, you can see a `<html>` tag.  Everything in the website is contained by this tag, and the last line of your entire document will always be `</html>`.

Inside `<html>`, there are two elements: `<head>`and `<body>`. Contained in `<head></head>`, we will put all kinds of information for the browser that the user doesn't necessarily need to see.  For now, we just have `<title>`. The content of `<title>` will be used for the name of the tab of the browser, and also by search engines. 

On the other side of the planet, we have `<body></body>`.  Everything visible to the user is contained in these tags.  Right now, all that consists of is "Hello, programmer!".  Replace this content with your own text in your favorite HTML editor, and then open the page in your browser.  Tada!

### Text Structure

Let's see some new tags for structuring your text. We will see more tags here.

Check out page2.html in the **Structure** folder.  The tags that we'll be talking about here are `<h1>`, `<p>`, `<ul>`, and `<li>`.  Open the file in the browser to try and understand. 

Now, let's see further.

First, we have `<h1>`, which adds a *heading* to our website.  Basically, a heading is just text with a bigger font.  But still.  Important. We'll soon learn how to adjust any and all font sizes, but not yet.  Just know that your headings should be in `<h1>` tags.  Also, if you have a smaller heading, or *sub-heading*, you could use `<h2>`, which is smaller than `<h1>`, but bigger than regular text.  You can keep going with more numbers until you reach `<h6>`, with each heading a bit smaller than the previous.  Try adding some subheadings underneath our current heading!

Next, we have `<p>` tags.  `<p>` adds a *paragraph* of text to our website, which are blocks of text that have some space before and after them.  Edit the text in the paragraphs given, and add your own to see what I mean!

And finally, we have `<ul>`.  `<ul>` means a bulleted list (also known as an *unordered list*), where every `<li>` is an item in that list (called a *list item*). But what if you want a numbered list?  You could change `<ul>` to `<ol>` (and don't forget its closing tag), it's that simple!  `<ol>` is an *ordered list*, which has numbers instead of bullet points, and that is truly the only difference.  Add some list items (`<li>`) to the list (make sure you stay inside the `<ul>` tags), and then change your `<ul>` tags to `<ol>`!

### Links

Links are made with the `<a>` tag, which stands for *anchor*.  

Open up the **Tags** folder, and add this piece of code right after your heading in page1.html:

```html
<p>This paragraph <a href="www.google.com">This is just a google home page link.</a></p>
```

Open <b>page1.html</b> in a browser and click on it!

Okay, so let's take a look at this.  First of all, you can see the `<a>` tag there contained in the paragraph.  Beautiful.
But what's that funky milk `href=`?  Well, that syntax called an *attribute*.  Attributes change the way a tag works, and are not visible to the website's user.  You only add attributes to the opening tag, not a closing tag.  Tags can have multiple attributes, for example:

```html
<tag attribute="value1" attribute2="value2">Content of tag</tag>`
```


#### Adding links to other pages in your website
If we have any website which describes Home, Contact. The links can be rendered in this way.

Normally when a beginner links to different pages on their website, they just make links that look like `<a href="http://sample.com/index.htmL">Home</a>` and `<a href="http://www.sample.com/contactus.htmL">Contact Us</a>`.

When you make a link to a page within your own directory or folder on your website, instead of putting in the whole URL, put in something more like this:

```html
<a href="page2.html">Click here to go back to Page 2.</a>
```


### Images
`<img>`. Let's just say you want to put an image on your website.  This is probably a good tag to know.  
Add the following to page1.html:

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fwallpaperaccess.com%2Ffull%2F550371.jpg&imgrefurl=https%3A%2F%2Fwallpaperaccess.com%2Ftulip&tbnid=FR4p93QnMuB7LM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygCegUIARDKAg..i&docid=hM_cVf0Q1H1w9M&w=1920&h=1200&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygCegUIARDKAg" />
```

Open up the page in a browser.  WHOA.  Image!  So, the `<img>` tag is one of those special tags.  First of all, it doesn't have a closing tag.  You just stick in a `/` at the end of the one tag and you're done.  Secondly, it also has a `src` attribute (which is short for *source*), and in the value of that attribute you put the URL of the image (similar to `href` in the anchor tag).

One attribute that might be good for you to remember for `<img>` tags is the `alt` attribute.  If you changed the code above to:

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" alt="These are tulip flowers" />
```

When you load the page in the browser, the image looks the same.  But, if you roll your mouse over the image, you'll see some words appear!. That's the `alt` attribute.  It stands for the *alternate text* for an image, and it's used when a user can't view the image for whatever reason (using a screen reader, slow connection, error in the `src` attribute, etc.).

### Line breaks
Let's just say you want to keep all your content in one paragraph `<p>`, but you still want to break it up.

That's easy.

So, there's two special tags here, `<hr>` and `<br>`.  They are *empty tags*, meaning they have no closing tag.

`<hr>` stands for *horizontal rule*, and creates a visible line break.
`<br>` is a simple line break, all it does is split your paragraph up.

Try inserting these in between some of your `<p>` tags to try it out!

### Tables
Open up sampleTables.html (in the **Tags**  folder) in a browser to check out the example table I made for you there.

There's several tags for tables, but the essential ones are `<table>`, `<tr>`, `<th>`, and `<td>`.  Look at sampleTables.html in your editor.

We're going to make our own table again on this page.  You can delete the one I made for you, or just make one underneath the current one there.

So, to create a table, you start with the `<table>` tag.  Simple enough.
	
This will contain all the parts of your table.  Sometimes, tables have a `border` attribute that will equal some value for the thickness of the table's border (it's proper to have just "1" or nothing, for reasons we'll explain later).  Go ahead and add one so it looks like this:

```html
<table border="1">
</table>
```


The next tag we're gonna check out is `<tr>`, which is for a *table row*.  Easy peasy.  So, let's add 3 `<tr>` tags to our table.

```html
<table border="1">
	<tr>
	</tr>
	<tr>
	</tr>
	<tr>
	</tr>
</table>
```

And finally, we have the actual cells of the table.  There are two types of tags for this, `<th>` (*table header*) and `<td>` (*table data*).  As their names indicate, the former is for the header of the table and the latter is for all of the data in the table.

In our first set of `<tr>` tags, add 4 `<th>` tags, and in the second and third `<tr>` tags add 4 `<td>` tags.

```html
<table border="1">
	<tr>
		<th></th>
		<th></th>
		<th></th>
		<th></th>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
	</tr>
</table>
```
	
Alright!  Our table is all set up.  We have a table with a `border=1` attribute, 3 rows, and 4 columns.  Let's populate it with data so you can see a proper application of the `<table>` tag:

```html
<table border="1">
	<tr>
		<th>Item</th>
		<th>Quantity</th>
		<th>Rate</th>
		<th>Cost</th>
	</tr>
	<tr>
		<td>oompa loompa - 1</td>
		<td>20</td>
		<td>1</td>
		<td>20.00</td>
	</tr>
	<tr>
		<td>oompa loompa - 2</td>
		<td>30</td>
		<td>2.00</td>
		<td>60.00</td>
	</tr>
</table>
```
	
Open the page in a browser and check out your work.

One other fun thing you can try playing with are the `colspan` and `rowspan` attributes.  If you add `colspan="2"` (or `rowspan`, or any other number) into a `<th>` or `<td>` tag, the cell will expand past their cell size.  For example, `<th colspan="2">` will give you a table header that spans 2 columns, and `<td rowspan="3">` will yield a cell that is the height of 3 rows.

You can also nest tables, but I won't get into that right now.  If you want to play around with the code, try adding some `<tr>` and `<td>` tags inside your current `<td>` tags.


### Colors

Open up the **Styles**  folder and the file style1.html. Look and feel of the page can be changed and this is how we gonna do it.

Add this line of code in the `<body>` somewhere below the header tags  `<p style="color: red">This text is hot like my body</p>`


The first thing we'll look at is the `style` attribute.  You can style all kind of things in that, from colors to widths to heights to borders to weights.  But for now, let's just talk color.


How do you get a specific color of your liking?  Well that's when you use RGB or HEX colors.  This is kind of a pain to grasp, it took me a little bit, so I'll explain it as simply as I can:  RGB stands for Red, Green, and Blue.  You can have the values 0 to 255 in each to form pretty much any color in existance.  Whoa.  The way to form an RGB code similarly to the one above is simple: `style="color: rgb(255,0,0)"`.  In this example, there's 255 reds, 0 greens, and 0 blues.  So, it's all red.  Boom, simple enough.

Now HEX colors is very similar.  It consists of the hashtag sign `#`, and then 6 *hexadecimal digits*, which are 0123456789ABCDEF, with F being the highest digit.  Like RGB, the first two digits of HEX are reds, the second two digits are blues, and the third couple of digits are greens.  So, to write the same color code above, you'd do `style="color: #FF0000"` to get red, because you have FF for reds, 00 for blues, and 00 for greens. 

There's plenty of websites and programs and color pickers out there to help you with that.  Here's a few:

 * [Color Picker](http://www.colorpicker.com/)
 * [HTML Color Picker](http://www.w3schools.com/colors/colors_picker.asp)

Try adding colors to various tags on the page!  You can make your `<h1>` the color `#005DFC`, your `<h3>` tag `rgb(242,127,56)`, and your `<p>` tag `lightblue`.


### Width and Height

There are two options you can use, the `style` attribute and the `width` and `height` attributes.  I'll show you both.

Take this block of code here and stick it into myStyles1.html:

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" />
```

Now, let's just say you want the image to be an exact size, say, 600x800.  All you need to do is add `width` and `height` attributes to do just that!

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" width="600" height="800" />
```

You'll notice that the proportions of the image are a little off.  That's actually pretty easy to fix.  Let's say that you absolutely have to have the width at 600 pixels, but the height can slide.  It's as easy as taking out the `height` attribute.

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" width="600" />
```

Refresh the page now. Same works for if you have a set height that you want, just include the `height` attribute and not the `width`.

Now, you can also do these changes with the `style` attribute.  

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" style="width: 600px" />
```

Simple enough!  Now, we've looked at the `style` attribute a bit now but I haven't explained the syntax.  The `style` attribute is for *inline styles*.  This means that you're styling your HTML directly in each element, rather than using CSS.  But, we haven't gotten that far yet, so I won't go into that part.

Now, the syntax within a `style` attribute is a little funky.  It is always `style="property: value"`, where the *property* is literally a property of the tag you're editing (for example, `color`, `width`, `height`), and the *value* is to what you're changing or editing the property (for example `blue`, `600px`, `#FF0000`).
If you have more than one property that you want to style, for example both height and width, you put a semicolon between delarations.  So, in our example, if you want to edit both height and width of our image in the `style` attribute, we'd do:

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" style="width: 600px; height: 800px" />
```


### Borders

What if we have a paragraph IN A BOX.  That's right.  Kind of like a table.  But not.  That'd be cool.  Of course, there are plenty of other things that can have a border.  Buttons (we'll get to those later), color blocks (also later), and images, and MORE can have them.  Mmmhm.

Let's take the same image we played with before:

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" />
```

Now, you can add `border="5"` to this and you'll get a border with a thickness of 5 pixels around the image.  But, this attribute is actually no longer supported for things other than tables (oh yeah, we used this for tables.  Memories.), so we can do this a better way.  You guessed it. `style` is coming to SAVE THE DAY.

The styling for borders with the `style` attribute is a bit different than just adding `border="5"`, but it's also much more powerful.  Let's change our code:

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fimg4.goodfon.com%2Fwallpaper%2Fnbig%2F4%2F6e%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.jpg&imgrefurl=https%3A%2F%2Fwww.goodfon.com%2Fwallpaper%2Fbeautiful-fresh-pink-tiulpany-tulips-buket-spring-flowers-ts.html&tbnid=XwTBtp2SwmXARM&vet=12ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg..i&docid=mGbi9yTtp8b4uM&w=1332&h=850&q=tulips&hl=en&ved=2ahUKEwjR3f3EteTqAhVQtKQKHbIuBc4QMygMegUIARDeAg" style="border:5px solid black" />
```


The first part of the declaration is obvious, `border`.  This is the property that we're editing.

Next, we have 3 parts in the value section.  The first part is `5px`.  Firstly, `px` stands for *pixels*.  We used this above for our width and heights as well.  You always have to include the units in your styling, and our units here are pixels.  Now, that whole first part, `5px`, is the border's thickness.  You guessed it: it's 5 pixels thick.  Gosh you're smart.
The next part is the *border style*.  You can plug in several words here, as indicated [on this webpage](http://www.w3schools.com/css/css_border.asp).  We used `solid`, but you can also say `dotted`, `dashed`, or `double`.  There are some other words you can use, but those depend on the color of the border.

Let's mix it up a bit with different borders for you to check out.  I'm just going to keep using the same image, you can replace it with whatever.  Stick this in the `<body>` tags of style1.html and check it out, and play with the values yourself!

```html
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Ftulipsinholland.com%2Fwp-content%2Fuploads%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland-2019-edition.png&imgrefurl=https%3A%2F%2Ftulipsinholland.com%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland%2F&tbnid=fUC5Kznjk3hv8M&vet=12ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ..i&docid=kEBMld7V7o_tjM&w=1170&h=490&q=tulips&ved=2ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ" style="border:5px dotted #ffcc00" />
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Ftulipsinholland.com%2Fwp-content%2Fuploads%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland-2019-edition.png&imgrefurl=https%3A%2F%2Ftulipsinholland.com%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland%2F&tbnid=fUC5Kznjk3hv8M&vet=12ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ..i&docid=kEBMld7V7o_tjM&w=1170&h=490&q=tulips&ved=2ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ" style="border:10px ridge rgb(77, 145, 99); width: 300px" />
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Ftulipsinholland.com%2Fwp-content%2Fuploads%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland-2019-edition.png&imgrefurl=https%3A%2F%2Ftulipsinholland.com%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland%2F&tbnid=fUC5Kznjk3hv8M&vet=12ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ..i&docid=kEBMld7V7o_tjM&w=1170&h=490&q=tulips&ved=2ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ" style="border:8px outset red" />	
<img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Ftulipsinholland.com%2Fwp-content%2Fuploads%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland-2019-edition.png&imgrefurl=https%3A%2F%2Ftulipsinholland.com%2F2019%2F01%2Fbest-place-to-stay-near-the-tulips-in-holland%2F&tbnid=fUC5Kznjk3hv8M&vet=12ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ..i&docid=kEBMld7V7o_tjM&w=1170&h=490&q=tulips&ved=2ahUKEwjM6KPjvOTqAhXBNuwKHeMNAEoQMyhEegUIARDvAQ" style="border:3px double #333a21; height: 30px" />
```			
			
Notice how I added `width` and `height` to a couple of them.  We're getting incestuous with our stylings.  Aww yeah.

### Text Styles

Besides having header tags and colors, there are other text styles that you can use.  What if you want bold text, or italics?  Different sizes?  Once again, the `style` attribute comes to the rescue.

Add the following to style1.html in **Styles**:

```html
<p style="text-align: center; font-weight: bold">This text is magnificent.</p>
```

Load that in a browser and check it out.  YUS.  You've got some magically centered, bolded text!  The properties defined here are pretty simple to follow.  `text-align` lets you align your text either `center`, `left`, or `right`.  Mess around with that so you get it.
`font-weight`, you guessed it, edits the weight in your text.  It can have the values `normal` for normally weighted text, `bold` for thick characters, `bolder` for thicker characters (specific, right?), `lighter` for lighter-weighted characters, and the numbers `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, and `900` (where 400 is the same as normal and 700 is the same as bold).

Play with this one now:

```html
<p style="font-family: Arial; font-style: italic">This text is magnificent.</p>
```

Browser time.  You've now got some text in the font Arial, and it's italic!
The properties we used here are `font-family` and `font-style`.  For the former, you can choose a lot of fonts, but you have to be careful.  Not every computer has the same fonts.  This is just my personal opinion: don't put something here besides Arial unless you've done some JavaScript magic.  And because I'm assuming you don't know JavaScript, don't use this unless you're changing this to Arial.  At least not yet. :)
And for `font-style`, it can be `normal`, `oblique`, and `italic`.

## Some More CSS

Open up your **Styles** folder again and open style2.html in your favorite editor.  This site is pretty barebones.  Let's take out the barebones part and just make it pretty.

We're going to be working in the `<head>` tag again.  Underneath the `<title>` tag, stick in the following:

```html
<style>
	body { }

	h1 { }

	h2 { }

	h3 { }

	h4 { }

	h5 { }

	h6 { }

	p { }

	ol { }
</style>
```

The `style` attribute is for styling *inline* HTML (just that line of code), the `<style>` tag is for holding CSS, and CSS *defines* the styles! 

Now, you'll notice some familiar keywords in there, in particular, `body`, `h1`, `p`, and `ol`.  That's right, they're the tags we know and love!  But, in CSS, these are called *selectors*.  The selector tells us what tag you're about to style.  So, whatever code you put in between the curly braces `{}` after the `body` selector will affect everything in the `<body>` tags.  Whatever you put in the braces after the `p` selector will affect what's in the `<p>` tags.
Whatever code you have in those curly braces will only affect that tag, so if you try editing the font colors for the `h1` selector, it won't affect whatever is in the `p` selector's tags.  Each portion of code `selector { code }` in CSS is called a *declaration*.  Make sense?  Good.  If not, keep reading and hopefully it will become more clear as we go on.

The code that we're going to be putting in each declaration is the same syntax as the code that we normally put in the `style` attribute.  How convenient.  So, change your code above to the following:

```html
<style>
	body {
		font-family: Arial;
	}

	h1 {
		color: red;
		text-align: center;
	}

	p {
		font-weight: bolder;
	}

	img {
		width: 400px;
		border: 5px solid #333333;
	}

	ol {
		color: #333333;
	}
</style>
```

For each selector, there is a *property* of that selector, and each property has a *value*, just like how we wrote it in the `style` attributes!

You will always have your CSS in the syntax, `selector { property: value; property: value; }`. 

Try playing around with the CSS we have right now.  Edit the colors, add some borders, change the font styles.  Don't forget your semicolons!

### Classes

Let's say that we have few `<p>` tags on our HTML page (hint: open myStyle3.html in the **Styles** folder).  
If we want to style each of these tags differently, we can use *classes*.  A class is actually an HTML attribute that you can name whatever you want.  
Check out myStyle3.html to see the classes I added to the `<p>` tags on the page.  When you add a class, the user doesn't see it.  
But, you can style specific classes to do what you want, instead of having all `<p>` tags be the same.

How about we style one of the classes specifically?  It's simple.  Just take the class name you made up (I'll use the `university` class for my example) and add a period `.` in front of it to select it in CSS, like so:



```css
p {
	font-family: Arial;
}
.university {
	font-weight: bolder;
}
.student {
	color: #555555;
}
.specs {
	font-style: italic;
}
```

### IDs

Now, let's talk about IDs.  They are very similar to classes.  The only real difference between classes and IDs is that you can only have one of each ID.  So, for example, if you have a special paragraph that you only want to style once, then you can stick in there the `id` attribute like so:

```html
<p id="special">Change the color of this text.</p>
```

When you want to style your IDs, you put a hashtag `#` before it in your CSS, like so:

```css
#special {

}
```
	
Remember:  You can only use an ID once.  IDs are more helpful when you're controlling the element with JavaScript, not styling, but that's something for another day.

#### Other important tags

Let's say that you want to separate individual text in your paragraphs or sections on your page.  Let's introduce 2 new tags: `<span>` and `<div>`.

##### The `<span>` tag
The `<span>` tag is pretty invisible unless you style it.  It's used to group *inline-elements* (so like a word in a paragraph), and it doesn't actually do anything unless you style or manipulate it with something else.

So, let's say you have a paragraph and you really want to emphasize some text within a paragraph without a line break or anything.  In comes `<span>`.  For example:

```html
<p>"My name is <span>Akshay Prasad</span> I'm a <span>master's student</span>" </p>
<p>~ Akshay Prasad </p>
```

In the above quote, you might want to style the `<span>` tags differently than the rest of the paragraph.  Maybe you want those words bold, or italics, or in red.  Now you can.

Add some `<span>` tags around your favorite lines of the poems in style3.html of the **Styles** folder.  Then, put the following CSS in your `<style>` tags:

```css
p span {
	font-style: italic;
}
```

```css
span {
	font-weight: bold;
}
.author span {
	color: #999999;
}
```

To sum up: `<span>` tags separate specific parts of paragraphs or other inline sections of a page.  They do nothing otherwise.  You can nest CSS if you want.

##### The `<div>` tag

The `<div>` tag is very similar to the `<span>` tag, in that it separates a section of something but doesn't do much else.  However, the difference with `<div>` tags is that they are <b>*block level*</b> elements, not just within a line of text.

The `<div>` tag might end up being the tag that you use most often.

Open up the **Layout** folder, and use your editor to open `homepage.html`.

```html
<!doctype html>
<html>
	<head>
		<title> My sample page </title>
		<style>

		</style>
	</head>
	<body>
		<div class="header"></div>
		<div class="menu"></div>
		<div class="content"></div>
		<div class="footer"></div>
	</body>
</html>
```

Besides the `<div>` tags, everything here should look familiar.  Each of the `<divs>` have a `class`, which means we should style those, right?  Right.

Within those `<style>` tags, let's add some more.  
First, let's throw in what we'll be styling: the `<html>` (it is unusual to style this, but I'll explain why we are later), `<body>`, and each of the 4 classes:

```css
html {

}
body {

}
.header {

}
.menu {

}
.content {

}
.footer {

}
```

This should be straightforward for you so far.  The first thing we'll do is create our layout by making each `<div>` a different size.

```css
html {
	height: 100%;
}
body {
	height: 100%;
}
.header {
	width: 100%;
	height: 60px;
}
.menu {
	height: 100%;
	width: 15%;
}
.content {
	height: 200px;
}
.footer {
	height: 60px;
	width: 100%;
}
```

Typically, the `height` property defaults to `0%` and the `width` property defaults to `100%`.  
This is why we had to style the `height` properties of both `<html>` and `<body>`.
If we had just made our `.menu` selector have a height of `100%`, we know that 100% of zero is just zero, so we wouldn't have a menu showing up!  
When we made the `<body>` tag have `height: 100%`, it also would still be zero, because our `<html>` tag also had a height of 0 without the CSS helping it out.
Now, if we had just said `height: 50px;` for `.menu`, we wouldn't need the `height` fixes for `<html>` and `<body>`, because it's given a set value, not a value dependent on others.  


Okay, so if you open `homepage.html` in the browser, you see nothing.  That's okay.  Let's change that by learning a few new CSS properties! 

##### Background color

One property that you will learn to know and love is `background-color`.  
It does exactly what you would expect it to: it sets the background color of the element it is styling!  
You can fill it in with HEX colors or RGB colors, just like we learned earlier, and the default color is white.

Let's add some backgrounds.

```css
html {
	height: 100%;
}
body {
	height: 100%;
}
.header {
	background-color: #99B5DD;
	width: 100%;
	height: 60px;
}
.menu {
	background-color: #DE90B1;
	height: 100%;
	width: 15%;
}
.content {
	height: 200px;
}
.footer {
	background-color: #0F215D;
	height: 60px;
	width: 100%;
}
```

Save in your editor and now refresh in that browser!.

##### Floating

One property that you will probably use fairly often is `float`.  
So, let's say that you want to have a picture in a paragraph.  When you see a picture in a news article or even a paper you're writing, the picture is either on the left or the right.  
It's the same in CSS!  If you wanted to put a picture in a paragraph, you'd make the `<img>` tag inside a `<p>` tag have the properties `float: left;` or `float: right;`.
So, what does this have to do with `<div>` tags?  Why could you potentially hate it?

With CSS float, a given element can be pushed to the left or right, allowing other elements to wrap around it.  
An element with `float` affecting it will move as far to the left or right as it can.  
Usually this means all the way to the left or right of the containing element.

Pretty simple, right?  Right.  Now, here's the cause for hate: sometimes, `float` just doesn't stop.  
It has the potential to mess up your layouts and have things move around other things, and really just give you a headache. 
How do you stop that?

With the `clear` property!  On the element(s) after any floated elements, make sure that they have `clear: both;` on them (we say `both` because it turns off both `left` and `right` floating).  
Let's add `float: left;` to the `.menu` and `.content` sections, and `clear: both;` to the `.footer`:

```css
html {
	height: 100%;
}
body {
	height: 100%;
}
.header {
	background-color: #99B5DD;
	width: 100%;
	height: 60px;
}
.menu {
	background-color: #DE90B1;
	height: 100%;
	width: 15%;
	float: left;
}
.content {
	height: 200px;
	float: left;
}
.footer	{
	background-color: #0F215D;
	height: 60px;
	width: 100%;
	clear: both;
}
```

Now if you refresh your browser, things will start appearing.

Let's add more!  So let's think, what if you're on your website, but you want to see the footer.  
You scroll down.  What if, though, you want to see the header again?  You'd have to scroll back up.


Let's make it so that your header and footer are always on the top and bottom of your screen, and only your content moves!

Incoming, the `position` property.

##### Positioning

The `position` property is pretty much exactly what one would expect a positioning property to do:  It positions things.

It can have several states, but we'll focus on the 3 states you'll probably use most: `absolute`, `relative`, and `fixed` (the default state is `static`, but you will rarely need to work with this).
 * In `absolute` positioning, the selected element will be placed in an exact location on the page, and moves with the page.  So, in our example, the header could be placed at the top of the page and the footer at the bottom, but when you scroll, they will move with the page and they won't stay where they are supposed to.  Some people like this, some don't.  In our case, we won't use this.
 * In `relative` positioning, the selected element will be placed *relative* (fancy that) to its default position.  I'll show you an example of this later.
 * Now, `fixed` positioning is just like `absolute` positioning, except that once an element is placed in an exact location on the page, it is stuck there.  A similar example is like a watermark on a video.  It stays the same there, no matter what the content is.

How do we actually position things after you use `position`?  You can use `top`, `bottom`, `left`, and `right` to place it.
So, for example, if you want a header bar to be at the top of the page (but it's okay if it scrolls with the page), you'll have `position: absolute;` and `top: 0px;` because you want it to be 0 pixels from the top.
If you have an image on your page that's sitting on the left of your document, but it's way too far left, you can do `position: relative;` and `left: 5px` to scoot it 5 pixels to the right (because you're adding space to the left).
Another more complicated example could be if, say, you want a 50px by 50px image to stay in the bottom right corner of your page as you scroll, you could do `position: fixed;` and `right: 50px;` and `bottom: 50px`.  You'll understand it more as we use it!

So, let's get rid of our `float` on `.menu` and `.content`, and the `clear` on the footer.  Let's position everything using `position` instead, like so:

```css
html {
	height: 100%;
}
body {
	height: 100%;
}
.header {
	background-color: #99c5dd;
	position: fixed;
	top: 0px;
	width: 100%;
	height: 60px;
}
.menu {
	background-color: #dd90b1;
	height: 100%;
	width: 15%;
	position: fixed;
	left: 0px;
	top: 60px;
}
.content {
	height: 200px;
	position: absolute;
	top: 60px;
	left: 15%;
}
.footer {
	background-color: #0f215d;
	position: fixed;
	bottom: 0px;
	height: 60px;
	width: 100%;
}
```
	
We are starting to look really hot now.  
If you refresh your page in the browser though, you'll notice that there's a little space to the left of our header and footer.  


##### Margins and Padding

![Alt](box_model.jpeg)

I made the diagram above to show you what the heck you'll be working with.

First, let's look at the CSS property `margin`.  Like you can see above, `margin` is the space *outside* the content's border.  
Think of it as the 1 inch margins when you write a paper, or the margins of the pages of a book.

The HTML `<body>` tag actually has a natural margin, which is why our header and footer have the space on their sides.  S
o, let's add `margin: 0px;` to our `<body>` (that's all we'll change right now though):

```css
body {
  font-family: 'Times New Roman', Times, serif;
  height: 100%;
  margin: 0px;
}
.header {
  background-color: #99c5dd;
  position: fixed;
  top: 0px;
  width: 100%;
  height: 60px;
  padding: 0px 10px;
  font-size: 50px;
  z-index: 10;
}
.menu {
  background-color: #dd90b1;
  height: 100%;
  width: 15%;
  position: fixed;
  left: 0px;
  top: 60px;
  padding: 10px 0px 0px;
  text-align: center;
  z-index: 5;
}
.content {
  height: 200px;
  position: absolute;
  top: 60px;
  left: 15%;
  padding: 10px;
  z-index: 0;
}
.footer {
  background-color: #0f215d;
  position: fixed;
  bottom: 0px;
  height: 60px;
  width: 100%;
  z-index: 10;
}

```

##### Z-Index

The property `z-index` isn't one that you'll run into super often, but it's something that will help you in the long run. 

Now, if you think of your screen as a stack of layers, like a stack of paper on the screen.  
Layer 1 is the lowest layer, and the higher the number, the higher the layer.

The numbers in `z-index` are the same.  If an element has `z-index: 0;`, then it is a bottom layer.  
If you have an element with a `z-index: 5;`, it's going to be on the 5th layer.

When you create a page and you don't add `z-index` to anything, the layers are just in order.  
So in our example, the `.header` was created first, so it's on the lowest layer, and the `.footer` was created last so it is on the top layer.

We don't want that.  What if your `.content` had a ton of information and you had to scroll the page?  
The content would overlap on top of the header (because we just HAD to make our header `fixed`).

So, let's add some `z-index` magic to our page!  A couple things to note first:

 * `z-index` only works when you have already set the `position` of an element.
 * You can assign any number you want to `z-index`, as long as it is an integer (no decimals), and as long as the highest number is the highest level, and the lowest number is the lowest level.

Okay, I'm going to add some `z-index` properties to the page, and I'm also going to add some text changes that you have seen before (`text-align`, `font-family`) and one that you haven't seen before (`font-size`... you get one guess to figure out what this does):

```css
html {
  height: 100%;
}
body {
  font-family: 'Times New Roman', Times, serif;
  height: 100%;
  margin: 0px;
}
.header {
  background-color: #99c5dd;
  position: fixed;
  top: 0px;
  width: 100%;
  height: 60px;
  padding: 0px 10px;
  font-size: 50px;
  z-index: 10;
}
.menu {
  background-color: #dd90b1;
  height: 100%;
  width: 15%;
  position: fixed;
  left: 0px;
  top: 60px;
  padding: 10px 0px 0px;
  text-align: center;
  z-index: 5;
}
.content {
  height: 200px;
  position: absolute;
  top: 60px;
  left: 15%;
  padding: 10px;
  z-index: 0;
}
.footer {
  background-color: #0f215d;
  position: fixed;
  bottom: 0px;
  height: 60px;
  width: 100%;
  z-index: 10;
}

```
Now you can see how flexible `<div>` tags really are.  You can style them pretty much any different way you want without breaking a sweat.

So, you have this delightful homepage set up now, try adding some content and play with the CSS a bit to make it your own!  Add colors, change sizes, the works.
When you click on the links to the other pages, About and Contact, you'll notice that they have no style right now (unlike you).Change that!  Try making your own layout for each of those pages.  If you're really digging what we've made here, that's cool too.  You can copy over the styles to each page.

### The `<link>` Tag, Comments

Let's just say you want to reuse your styles across your website on every page.  It makes sense.  
It'd be kind of annoying to have drastic changes on every page.

#### The `<link>` tag

That's where the `<link>` tag comes in!  The `<link>` tag is an empty tag (like <br> and <img>), so it has no end tag, and it's used to link to external stylesheets!

What the heck is an external stylesheet?  Well, put simply, it's CSS, in its own file.

You write the `<link>` tag like this:

```html
<link rel="stylesheet" type="text/css" href="main.css">
```

Let's take a look at those attributes.  The `rel` attribute is for *relationship*.  
It specifies the relationship between the current document and the linked document, which will almost always be `stylesheet`.  
I've never actually seen it in action with anything other than `stylesheet`, but if you really want to know other values you can look it up.
The `type` attribute will also pretty much always be `text/css`.  If it's ever anything else when you want to use it with CSS, I will be quite surprised.
And finally, `href`.  You remember this one, I hope!  It's just like our `<a>` tag.  It is the URL of the stylesheet.

Let's check out this `<link>` tag in action.  Open up the **Linking** folder and open home.html, and paste the `<link>` line above on the line below the `<title>` tags in the `<head>`.  Refresh your browser and check out the magic.  It should look just like what we made in the previous section!  
Now, if you open the main.css file in your editor, you'll see that it's all the CSS you recognize, but there's no `<style>` tags.  Those tags aren't needed when you are using a CSS file!

#### Commenting

Let's just say that you want to show off your code to someone, but they're not exactly sure what you're doing.  

You can add comments!

*Comments* in your code are blocks of text that will not be read by the computer.  Every computer language has them.

##### HTML Comments

In HTML, a comment looks like this:

```html
<!-- This is an HTML comment! -->
```

As you can see, it almost looks like a regular tag, with an opening `<!--` and an ending `-->`.  You can put this pretty much anywhere in your HTML files and it won't affect your work!

Look inside the **Overall** folder, and open index.html.  You'll see a few comments there.  Notice how you can put them all on one line, or in a multi-line block!  As long as you have a beginning `<!--` and end `-->`, you have total freedom with comments.

#### CSS Comments

A comment in CSS is similar to HTML in that it has a beginning and end part, but it looks a little different:

```css
/* This is a comment in CSS! */
```

Just like in the HTML comments, you have a beginning `/*` and an end `*/`.  
If you open up main.css in the **Project** folder, you can see the comments I wrote in there!  
And again, you can have single-line comments, and multi-line ones too.

Comments are great for keeping track of what you're doing, especially if a project you're working on spans over a period of time.  
You can make notes for yourself to check later, or you could just tell someone who is reading your code that they are attractive.


##### Forms

A common thing you'll see on websites are forms, like textboxes, buttons, and checkboxes.

If you're really dying to see a button, here you go:

```html
<button type="button">Click Me!</button>
```

And there you have it, a button on your website!  If you actually want to know how to make the button or form do something, you'll need to know some JavaScript.
Until you do, here's more information on buttons: [W3Schools - HTML Forms](http://www.w3schools.com/tags/tag_form.asp)

##### HTML5 and CSS3

If you've read anything about the internet and developing for it, you've probably heard some key words thrown around, and a couple of those key words are HTML5 and CSS3.
What are those, actually?  Well, HTML5 is the latest standard for HTML. It first came out in late 2014. The previous HTML version came out in 1999, which is quite a while ago. Unless you're time traveling right now and you printed this out to read as you go.

Anyway.  HTML5 was designed to deliver rich content without the need for additional plugins (for example, Shockwave Flash, Silverlight, etc.), and can handle everything from animation to graphics, music to movies, and can also be used to build complex web applications. 
Not to mention the fact that it works on every device, from tablets to phones to your standard computer.

CSS3 has a bunch of new features too.  From new selectors to fancy text effects to 2D/3D tranformations, there's just so much to learn!

If you ever are looking for a job or something, and they say "HTML5 and CSS3," you should know that all that means is "you're up to date on your HTML and CSS." All HTML and CSS these days is HTML5 and CSS3. If you've followed along this far, you are pretty up to date, and there's tons of resources out there on how to use more advanced features of both.

## Project!

Alrighty!  So you've looked at the **Overall** folder a bit, but I haven't told you what that folder is for yet.


It's a project. [Akshay]

Put a photo up of yourself, add a biography, talk about your skills (be sure to include HTML and CSS among them) and experiences, make it the online version of you.

Use `<div>` tags and CSS to make a really awesome layout.  Style everything in the text from `<h1>` to `<p>`.  

Include lists `<ul>` and links `<a>`!  Make it sparkly.

I made your homepage for you, and your main CSS document.  But don't let that limit you!  Add as much as you want, and experiment!

The best way to learn is by doing.  Do as much as you can until you think you have everything down.

## Signing off:
<b><i>Akshay Prasad</i></b> <br/>
<b>#Developer #TechEnthusiast #Agile #Agilelearning #scrum #scrumlearning #projectmanagement #software</b>
