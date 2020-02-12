# UofA Coding Bootcamp: Homework#1 (Code Refactor)

The goal of this assignment was to take an existing webpage and refactor the HTML and CSS to make it more efficient, without changing the actual layout or design of the webpage itself.

-----------------------------------------------------

Below, I list the changes made to the HTML and CSS pages:

-----------------------------------------------------

## changes made to HTML:
* comments added before each section
    * Lines: 7, 12, 29, 32, 56, 81
* changed the website title (Line 8) from "website" to "Horiseon"
* changes to < div > < / div > tags to reflect semantic HTML elements:
    * Lines 13 and 28: < div > < / div > tags changed to < header > < / header > tags tags
    * Lines 15 and 27: < div > < / div > tags changed to < nav > < / nav > tags, for "navigation"
    * Lines 30 and 80: < main > < / main > tags added to define to main content
    * Line 31: < div > < / div > tags changed to < section > < / section > tags tags to identify the image as its own section
    * Lines 33 and 55: < div >< / div > changed to < section > < / section > to identify the three articles as one section
    * Lines 34&40, 41&47, and 48&54: each pair of < div >< / div > tags changed to < article >< / article > tags to identify each of the three as separate subsections of content within one section
    * Lines 57 and 79: < div >< / div > changed to < aside >< / aside > to reflect that this section is a sidebar
    * Lines 58&64, 65&71, and 72&78: each pair of < div >< / div > tags changed to < article >< / article > tags to identify the three as separate subsections of content within one section
    Lines 82 and 87: < div >< / div > changed to < footer >< / footer > to identify this as the page footer
    Line 83: the < h2 >< / h2 > headings have been changed to < h4 >< / h4 > so that the headings throughout the page are sequential
* changes made to correct problems with HTML functions
    * Line 34: the id attribute is missing a class attribute, causing the page to be unable to render this link; class attribute has been added, reflecting the corresponding class selector in the CSS( seen as class="search-engine-optimization in the HTML now)
    * Line 35, 42, 49, 60, 67, and 74: alt attributes added to the images
    
    -----------------------------------------------------

## changes made to CSS:
* comments added before each section
    * Lines: 11, 46, 57, 78, 110, 142
* Line 29: ".header div" has been changed to ".header nav" to reflect the corresponding change in the HTML page
* Line 36: ".header div ul {list-style-type: none;}" deleted, as it has no affect on the webpage
* Line 37: ".header div ul li" changed to ".header nav ul li" to reflect the corresponding change in the HTML page
*  Lines 82-104: this block of CSS selectors and declarations have been moved from their original position (Lines 137-189 in the unaltered original CSS page) to here
    * In addition the selectors in this "main content section" can be consolidated significantly; they can be grouped into three subsections of content based on the identical declarations
    
    Before:
```    
.search-engine-optimization {
margin-bottom: 20px;
padding: 50px;
height: 300px;
font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
background-color: #0072bb;
color: #ffffff;
}

.online-reputation-management {
margin-bottom: 20px;
padding: 50px;
height: 300px;
font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
background-color: #0072bb;
color: #ffffff;
}

.social-media-marketing {
margin-bottom: 20px;
padding: 50px;
height: 300px;
font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
background-color: #0072bb;
color: #ffffff;
}

.search-engine-optimization img {
max-height: 200px;
}

.online-reputation-management img {
max-height: 200px;
}

.social-media-marketing img {
max-height: 200px;
}

.search-engine-optimization h2 {
margin-bottom: 20px;
font-size: 36px;
}

.online-reputation-management h2 {
margin-bottom: 20px;
font-size: 36px;
}

.social-media-marketing h2 {
margin-bottom: 20px;
font-size: 36px;
}
```

After:
```
.search-engine-optimization,
.online-reputation-management,
.social-media-marketing {
margin-bottom: 20px;
padding: 50px;
height: 300px;
font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
background-color: #0072bb;
color: #ffffff;
}

.search-engine-optimization img,
.online-reputation-management img,
.social-media-marketing img {
max-height: 200px;
}

.search-engine-optimization h2,
.online-reputation-management h2,
.social-media-marketing h2 {
margin-bottom: 20px;
font-size: 36px;
}
```
    
*  Lines 108-115: this ".benefits" class selector contains two irrelevent declarations that have been deleted: "clear: both" and "height: 100%"
* Lines 117-136: this block of CSS selectors and declarations (reflected in the < aside >< / aside > tags in the HTML and the sidebar in the webpage) can also be consolidated into three sections based on their identical declarations

Before:
```
.benefit-lead {
margin-bottom: 32px;
color: #ffffff;
}

.benefit-brand {
margin-bottom: 32px;
color: #ffffff;
}

.benefit-cost {
margin-bottom: 32px;
color: #ffffff;
}

.benefit-lead h3 {
margin-bottom: 10px;
text-align: center;
}

.benefit-brand h3 {
margin-bottom: 10px;
text-align: center;
}

.benefit-cost h3 {
margin-bottom: 10px;
text-align: center;
}

.benefit-lead img {
display: block;
margin: 10px auto;
max-width: 150px;
}

.benefit-brand img {
display: block;
margin: 10px auto;
max-width: 150px;
}

.benefit-cost img {
display: block;
margin: 10px auto;
max-width: 150px;
}
```

After:
```
.benefit-lead,
.benefit-brand,
.benefit-cost {
margin-bottom: 32px;
color: #ffffff;
}

.benefit-lead h3,
.benefit-brand h3,
.benefit-cost h3 {
text-align: center;
}

.benefit-lead img,
.benefit-brand img,
.benefit-cost img {
display: block;
margin: 10px auto;
max-width: 150px;
}
```

* Line 147: ".footer h2" has been changed to ".footer h4" to reflect the corresponding change in the HTML page

-----------------------------------------------------

# URLs:
* deployed application: https://CrainDavis.github.io/Homework-1/
* GitHub Repository: https://github.com/CrainDavis/Homework-1.git
