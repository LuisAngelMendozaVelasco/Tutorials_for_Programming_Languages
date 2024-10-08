# Layout

## Layout using float

Code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>CSS Template</title>
        <meta charset="utf-8" name="viewport" content="width=device-width, initial-scale=1">
        <style>
            * {box-sizing: border-box;}

            body {font-family: Arial, Helvetica, sans-serif;}

            /* Style the header */
            header {background-color: #666;
                    padding: 30px;
                    text-align: center;
                    font-size: 35px;
                    color: white;}

            /* Create two columns/boxes that floats next to each other */
            nav {   float: left;
                    width: 30%;
                    height: 300px; /* only for demonstration, should be removed */
                    background: #ccc;
                    padding: 20px;}

            /* Style the list inside the menu */
            nav ul {list-style-type: none;
                    padding: 0;}

            article {   float: left;
                        padding: 20px;
                        width: 70%;
                        background-color: #f1f1f1;
                        height: 300px;} /* only for demonstration, should be removed */

            /* Clear floats after the columns */
            section::after {content: "";
                            display: table;
                            clear: both;}

            /* Style the footer */
            footer {background-color: #777;
                    padding: 10px;
                    text-align: center;
                    color: white;}

            /* Responsive layout - makes the two columns/boxes stack on top of each other instead of next to each other, on small screens */
            @media (max-width: 600px) { nav, article {  width: 100%;
                                                        height: auto;}}
        </style>
    </head>
    <body>
        <h2>CSS Layout Float</h2>
        <p>In this example, we have created a header, two columns/boxes and a footer. On smaller screens, the columns will stack on top of each other.</p>
        <p>Resize the browser window to see the responsive effect (you will learn more about this in our next chapter - HTML Responsive.)</p>

        <header>
            <h2>Cities</h2>
        </header>

        <section>
            <nav>
                <ul>
                    <li><a href="#">London</a></li>
                    <li><a href="#">Paris</a></li>
                    <li><a href="#">Tokyo</a></li>
                </ul>
            </nav>
            
            <article>
                <h1>London</h1>
                <p>London is the capital city of England. It is the most populous city in the  United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
                <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
            </article>
        </section>

        <footer>
            <p>Footer</p>
        </footer>
    </body>
</html>
```

Output:

[Click here!](./Layout/Example_1.html)

## Layout using flexbox

Code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>CSS Template</title>
        <meta charset="utf-8" name="viewport" content="width=device-width, initial-scale=1">
        <style>
            * {box-sizing: border-box;}

            body {font-family: Arial, Helvetica, sans-serif;}

            /* Style the header */
            header {background-color: #666;
                    padding: 30px;
                    text-align: center;
                    font-size: 35px;
                    color: white;}

            /* Container for flexboxes */
            section {   display: -webkit-flex;
                        display: flex;}

            /* Style the navigation menu */
            nav {   -webkit-flex: 1;
                    -ms-flex: 1;
                    flex: 1;
                    background: #ccc;
                    padding: 20px;}

            /* Style the list inside the menu */
            nav ul {list-style-type: none;
                    padding: 0;}

            /* Style the content */
            article {   -webkit-flex: 3;
                        -ms-flex: 3;
                        flex: 3;
                        background-color: #f1f1f1;
                        padding: 10px;}

            /* Style the footer */
            footer {background-color: #777;
                    padding: 10px;
                    text-align: center;
                    color: white;}

            /* Responsive layout - makes the menu and the content (inside the section) sit on top of each other instead of next to each other */
            @media (max-width: 600px) {section {-webkit-flex-direction: column;
                                                flex-direction: column;}}
        </style>
    </head>
    <body>
        <h2>CSS Layout Flexbox</h2>
        <p>In this example, we have created a header, two columns/boxes and a footer. On smaller screens, the columns will stack on top of each other.</p>
        <p>Resize the browser window to see the responsive effect.</p>
        <p><strong>Note:</strong> Flexbox is not supported in Internet Explorer 10 and earlier versions.</p>

        <header>
            <h2>Cities</h2>
        </header>

        <section>
            <nav>
                <ul>
                    <li><a href="#">London</a></li>
                    <li><a href="#">Paris</a></li>
                    <li><a href="#">Tokyo</a></li>
                </ul>
            </nav>
            
            <article>
                <h1>London</h1>
                <p>London is the capital city of England. It is the most populous city in the  United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
                <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
            </article>
        </section>

        <footer>
            <p>Footer</p>
        </footer>
    </body>
</html>
```

Output:

[Click here!](./Layout/Example_2.html)

## Layout using flexbox 2

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style> 
            .flex-container {   display: -webkit-flex;
                                display: flex;  
                                -webkit-flex-flow: row wrap;
                                flex-flow: row wrap;
                                font-weight: bold;
                                text-align: center;}

            .flex-container > * {   padding: 10px;
                                    flex: 1 100%;}

            .main { text-align: left;
                    background: cornflowerblue;}

            .header {background: coral;}
            .footer {background: lightgreen;}
            .aside {background: moccasin;}

            @media all and (min-width: 768px) { .aside  { flex: 1 auto; }
                                                .main   { flex: 3 0px; }
                                                .aside  { order: 1; } 
                                                .main   { order: 2; }
                                                .footer { order: 4; }}
        </style>
    </head>
    <body>
        <div class="flex-container">
            <header class="header">Header</header>
            <aside class="aside">Aside</aside>
            <article class="main">
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque sed ex turpis. Cras luctus nibh lectus, in ullamcorper ex tempor eleifend. Nulla bibendum, eros a consequat vestibulum, orci massa fermentum quam, sed commodo nunc ex vitae nisl. Aliquam ullamcorper interdum est nec tincidunt.</p>
            </article>
            <footer class="footer">Footer</footer>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Layout/Example_3.html)

## Layout using flexbox 3

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style> 
            .flex-container {   display: -webkit-flex;
                                display: flex;  
                                -webkit-flex-flow: row wrap;
                                flex-flow: row wrap;
                                font-weight: bold;
                                text-align: center;}

            .flex-container > * {   padding: 10px;
                                    flex: 1 100%;}

            .main { text-align: left;
                    background: cornflowerblue;}

            .header {background: coral;}
            .footer {background: lightgreen;}
            .aside1 {background: moccasin;}
            .aside2 {background: violet;}

            @media all and (min-width: 768px) { .aside  { flex: 1 auto; }
                                                .main   { flex: 3 0px; }
                                                .aside1 { order: 1; } 
                                                .main   { order: 2; }
                                                .aside2 { order: 3; }
                                                .footer { order: 4; }}
        </style>
    </head>
    <body>
        <div class="flex-container">
            <header class="header">Header</header>
            <aside class="aside aside1">Aside 1</aside>
            <article class="main">
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque sed ex turpis. Cras luctus nibh lectus, in ullamcorper ex tempor eleifend. Nulla bibendum, eros a consequat vestibulum, orci massa fermentum quam, sed commodo nunc ex vitae nisl. Aliquam ullamcorper interdum est nec tincidunt.</p>
            </article>
            <aside class="aside aside2">Aside 2</aside>
            <footer class="footer">Footer</footer>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Layout/Example_4.html)