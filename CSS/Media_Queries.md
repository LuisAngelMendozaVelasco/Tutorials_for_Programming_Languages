# Media Queries

## Change the background-color to lightgreen if the viewport is 480px wide or wider

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            body {background-color: pink;}

            @media screen and (min-width: 480px) {body {background-color: lightgreen;}}
        </style>
    </head>
    <body>
        <h1>Resize the browser window to see the effect!</h1>
        <p>The media query will only apply if the media type is screen and the viewport is 480px wide or wider.</p>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_1.html)

## Show a menu that will float to the left of the page if the viewport is 480px wide or wider

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <style>
            .wrapper {overflow: auto;}

            #main {margin-left: 4px;}

            #leftsidebar {  float: none;
                            width: auto;}

            #menulist { margin: 0;
                        padding: 0;}

            .menuitem { background: #CDF0F6;
                        border: 1px solid #d4d4d4;
                        border-radius: 4px;
                        list-style-type: none;
                        margin: 4px;
                        padding: 2px;}

            @media screen and (min-width: 480px) {  #leftsidebar {width: 200px; float: left;}
                                                    #main {margin-left: 216px;}}
        </style>
    </head>
    <body>
        <div class="wrapper">
            <div id="leftsidebar">
                <ul id="menulist">
                    <li class="menuitem">Menu-item 1</li>
                    <li class="menuitem">Menu-item 2</li>
                    <li class="menuitem">Menu-item 3</li>
                    <li class="menuitem">Menu-item 4</li>
                    <li class="menuitem">Menu-item 5</li>
                </ul>
            </div>
            
            <div id="main">
                <h1>Resize the browser window to see the effect!</h1>
                <p>This example shows a menu that will float to the left of the page if the viewport is 480 pixels wide or wider. If the viewport is less than 480 pixels, the menu will be on top of the content.</p>
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_2.html)

## Set different background colors depending on screen width

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            body {  background-color: tan;
                    color: black;}

            /* On screens that are 992px wide or less, the background color is blue */
            @media screen and (max-width: 992px) {body {background-color: blue;
                                                        color: white;}}

            /* On screens that are 600px wide or less, the background color is olive */
            @media screen and (max-width: 600px) {body {background-color: olive;
                                                        color: white;}}
        </style>
    </head>
    <body>
        <h1>Resize the browser window to see the effect!</h1>
        <p>By default, the background color of the document is "tan". If the screen size is 992px or less, the color will change to "blue". If it is 600px or less, it will change to "olive".</p>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_3.html)

## Responsive navigation menu

Code: 

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            * {box-sizing: border-box;}

            /* Style the top navigation bar */
            .topnav {   overflow: hidden;
                        background-color: #333;}

            /* Style the topnav links */
            .topnav a { float: left;
                        display: block;
                        color: #f2f2f2;
                        text-align: center;
                        padding: 14px 16px;
                        text-decoration: none;}

            /* Change color on hover */
            .topnav a:hover {   background-color: #ddd;
                                color: black;}

            /* On screens that are 600px wide or less, make the menu links stack on top of each other instead of next to each other */
            @media screen and (max-width: 600px) {.topnav a {   float: none;
                                                                width: 100%;}}
        </style>
    </head>
    <body>
        <h2>Responsive navigation menu</h2>
        <p>Resize the browser window to see the effect: When the screen is less than 600px, the navigation menu will be displayed vertically instead of horizontally.</p>

        <div class="topnav">
            <a href="#">Link</a>
            <a href="#">Link</a>
            <a href="#">Link</a>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_4.html)

## Responsive columns using float

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            * {box-sizing: border-box;}

            /* Create four equal columns that floats next to each other */
            .column {   float: left;
                        width: 25%;
                        padding: 20px;}

            /* Clear floats after the columns */
            .row:after {content: "";
                        display: table;
                        clear: both;}

            /* On screens that are 992px wide or less, go from four columns to two columns */
            @media screen and (max-width: 992px) {.column {width: 50%;}}

            /* On screens that are 600px wide or less, make the columns stack on top of each other instead of next to each other */
            @media screen and (max-width: 600px) {.column {width: 100%;}}
        </style>
    </head>
    <body>
        <h2>Responsive Four Column Layout</h2>
        <p><strong>Resize the browser window to see the responsive effect.</strong> On screens that are 992px wide or less, the columns will resize from four columns to two columns. On screens that are 600px wide or less, the columns will stack on top of each other instead of next to eachother.</p>

        <div class="row">
            <div class="column" style="background-color:#aaa;">
                <h2>Column 1</h2>
                <p>Some text..</p>
            </div>
            
            <div class="column" style="background-color:#bbb;">
                <h2>Column 2</h2>
                <p>Some text..</p>
            </div>
            
            <div class="column" style="background-color:#ccc;">
                <h2>Column 3</h2>
                <p>Some text..</p>
            </div>
            
            <div class="column" style="background-color:#ddd;">
                <h2>Column 4</h2>
                <p>Some text..</p>
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_5.html)

## Responsive columns using flexbox

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            * {box-sizing: border-box;}

            /* Container for flexboxes */
            .row {  display: flex;
                    flex-wrap: wrap;}

            /* Create four equal columns */
            .column {   flex: 25%;
                        padding: 20px;}

            /* On screens that are 992px wide or less, go from four columns to two columns */
            @media screen and (max-width: 992px) {.column {flex: 50%;}}

            /* On screens that are 600px wide or less, make the columns stack on top of each other instead of next to each other */
            @media screen and (max-width: 600px) {.row {flex-direction: column;}}
        </style>
    </head>
    <body>
        <h2>Responsive Four Column Layout with Flex</h2>
        <p><strong>Resize the browser window to see the responsive effect.</strong> On screens that are 992px wide or less, the columns will resize from four columns to two columns. On screens that are 600px wide or less, the columns will stack on top of each other instead of next to eachother.</p>

        <div class="row">
            <div class="column" style="background-color:#aaa;">
                <h2>Column 1</h2>
                <p>Some text..</p>
            </div>
            
            <div class="column" style="background-color:#bbb;">
                <h2>Column 2</h2>
                <p>Some text..</p>
            </div>
            
            <div class="column" style="background-color:#ccc;">
                <h2>Column 3</h2>
                <p>Some text..</p>
            </div>
            
            <div class="column" style="background-color:#ddd;">
                <h2>Column 4</h2>
                <p>Some text..</p>
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_6.html)

## Hide elements with media queries

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            div.example {   background-color: yellow;
                            padding: 20px;}

            @media screen and (max-width: 600px) {div.example {display: none;}}
        </style>
    </head>
    <body>
        <h2>Hide elements on different screen sizes</h2>

        <div class="example">Example DIV.</div>

        <p>When the browser's width is 600px wide or less, hide the div element. Resize the browser window to see the effect.</p>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_7.html)

## Responsive font size

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            div.example {   background-color: lightgrey;
                            padding: 20px;}

            @media screen and (min-width: 600px) {div.example {font-size: 80px;}}

            @media screen and (max-width: 600px) {div.example {font-size: 30px;}}
        </style>
    </head>
    <body>
        <h2>Change the font size of an element on different screen sizes</h2>

        <div class="example">Example DIV.</div>

        <p>When the browser's width is 600px wide or less, set the font-size of DIV to 30px. When it is 601px or wider, set the font-size to 80px. Resize the browser window to see the effect.</p>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_8.html)

## Responsive image gallery

Code: 

```html
<!DOCTYPE html>
<html>
    <style>
        * {box-sizing: border-box;}

        body {  margin: 0;
                font-family: Arial;}

        .header {   text-align: center;
                    padding: 32px;}

        .row {  display: flex;
                flex-wrap: wrap;
                padding: 0 4px;}

        /* Create four equal columns that sits next to each other */
        .column {   flex: 25%;
                    max-width: 25%;
                    padding: 0 4px;}

        .column img {   margin-top: 8px;
                        vertical-align: middle;}

        /* Responsive layout - makes a two column-layout instead of four columns */
        @media screen and (max-width: 800px) {.column { flex: 50%;
                                                        max-width: 50%;}}

        /* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
        @media screen and (max-width: 600px) {.column { flex: 100%;
                                                        max-width: 100%;}}
    </style>
    <body>
        <!-- Header -->
        <div class="header">
            <h1>Responsive Image Grid</h1>
            <p>Resize the browser window to see the responsive effect.</p>
        </div>

        <!-- Photo Grid -->
        <div class="row"> 
            <div class="column">
                <img src="../data/images/wedding.jpg" style="width:100%">
                <img src="../data/images/rocks.jpg" style="width:100%">
                <img src="../data/images/falls2.jpg" style="width:100%">
                <img src="../data/images/paris.jpg" style="width:100%">
                <img src="../data/images/nature.jpg" style="width:100%">
                <img src="../data/images/mist.jpg" style="width:100%">
                <img src="../data/images/paris.jpg" style="width:100%">
            </div>
            
            <div class="column">
                <img src="../data/images/underwater.jpg" style="width:100%">
                <img src="../data/images/ocean.jpg" style="width:100%">
                <img src="../data/images/wedding.jpg" style="width:100%">
                <img src="../data/images/mountainskies.jpg" style="width:100%">
                <img src="../data/images/rocks.jpg" style="width:100%">
                <img src="../data/images/underwater.jpg" style="width:100%">
            </div> 
            
            <div class="column">
                <img src="../data/images/wedding.jpg" style="width:100%">
                <img src="../data/images/rocks.jpg" style="width:100%">
                <img src="../data/images/falls2.jpg" style="width:100%">
                <img src="../data/images/paris.jpg" style="width:100%">
                <img src="../data/images/nature.jpg" style="width:100%">
                <img src="../data/images/mist.jpg" style="width:100%">
                <img src="../data/images/paris.jpg" style="width:100%">
            </div>
            
            <div class="column">
                <img src="../data/images/underwater.jpg" style="width:100%">
                <img src="../data/images/ocean.jpg" style="width:100%">
                <img src="../data/images/wedding.jpg" style="width:100%">
                <img src="../data/images/mountainskies.jpg" style="width:100%">
                <img src="../data/images/rocks.jpg" style="width:100%">
                <img src="../data/images/underwater.jpg" style="width:100%">
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_9.html)

## Responsive website

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            * {box-sizing: border-box;}

            /* Style the body */
            body {  font-family: Arial;
                    margin: 0;}

            /* Header/logo Title */
            .header {   padding: 60px;
                        text-align: center;
                        background: #1abc9c;
                        color: white;}

            /* Style the top navigation bar */
            .navbar {   display: flex;
                        background-color: #333;}

            /* Style the navigation bar links */
            .navbar a { color: white;
                        padding: 14px 20px;
                        text-decoration: none;
                        text-align: center;}

            /* Change color on hover */
            .navbar a:hover {   background-color: #ddd;
                                color: black;}

            /* Column container */
            .row {  display: flex;
                    flex-wrap: wrap;}

            /* Create two unequal columns that sits next to each other */
            /* Sidebar/left column */
            .side { flex: 30%;
                    background-color: #f1f1f1;
                    padding: 20px;}

            /* Main column */
            .main { flex: 70%;
                    background-color: white;
                    padding: 20px;}

            /* Fake image, just for this example */
            .fakeimg {  background-color: #aaa;
                        width: 100%;
                        padding: 20px;}

            /* Footer */
            .footer {   padding: 20px;
                        text-align: center;
                        background: #ddd;}

            /* Responsive layout - when the screen is less than 700px wide, make the two columns stack on top of each other instead of next to each other */
            @media screen and (max-width: 700px) {.row, .navbar {flex-direction: column;}}
        </style>
    </head>
    <body>
        <!-- Note -->
        <div style="background:yellow;padding:5px">
            <h4 style="text-align:center">Resize the browser window to see the responsive effect.</h4>
        </div>

        <!-- Header -->
        <div class="header">
            <h1>My Website</h1>
            <p>With a <b>flexible</b> layout.</p>
        </div>

        <!-- Navigation Bar -->
        <div class="navbar">
            <a href="#">Link</a>
            <a href="#">Link</a>
            <a href="#">Link</a>
            <a href="#">Link</a>
        </div>

        <!-- The flexible grid (content) -->
        <div class="row">
            <div class="side">
                <h2>About Me</h2>
                <h5>Photo of me:</h5>
                <div class="fakeimg" style="height:200px;">Image</div>
                <p>Some text about me in culpa qui officia deserunt mollit anim..</p>
                <h3>More Text</h3>
                <p>Lorem ipsum dolor sit ame.</p>
                <div class="fakeimg" style="height:60px;">Image</div><br>
                <div class="fakeimg" style="height:60px;">Image</div><br>
                <div class="fakeimg" style="height:60px;">Image</div>
            </div>
            
            <div class="main">
                <h2>TITLE HEADING</h2>
                <h5>Title description, Dec 7, 2017</h5>
                <div class="fakeimg" style="height:200px;">Image</div>
                <p>Some text..</p>
                <p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
                <br>
                <h2>TITLE HEADING</h2>
                <h5>Title description, Sep 2, 2017</h5>
                <div class="fakeimg" style="height:200px;">Image</div>
                <p>Some text..</p>
                <p>Sunt in culpa qui officia deserunt mollit anim id est laborum consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.</p>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <h2>Footer</h2>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_10.html)

## Change layout of a page depending on the orientation of the browser

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <style>
            body {background-color: lightgreen;}

            @media only screen and (orientation: landscape) {body {background-color: lightblue;}}
        </style>
    </head>
    <body>
        <p>Resize the browser window. When the width of this document is larger than the height, the background color is "lightblue", otherwise it is "lightgreen".</p>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_11.html)

## Min width to max width

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <style>
            @media screen and (max-width: 900px) and (min-width: 600px) {div.example {  font-size: 50px;
                                                                                        padding: 50px;
                                                                                        border: 8px solid black;
                                                                                        background: yellow;}}
        </style>
    </head>
    <body>
        <h2>Change the appearance of DIV on different screen sizes</h2>

        <div class="example">Example DIV.</div>

        <p>When the browser's width is between 600 and 900px, change the appearance of DIV. 
        <strong>Resize the browser window to see the effect</strong>.</p>
    </body>
</html>
```

Output:

[Click here!](./Media_Queries/Example_12.html)