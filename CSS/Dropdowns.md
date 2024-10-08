# Dropdowns

## Dropdown text

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .dropdown { position: relative;
                        display: inline-block;}

            .dropdown-content { display: none;
                                position: absolute;
                                background-color: #f9f9f9;
                                min-width: 160px;
                                box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
                                padding: 12px 16px;
                                z-index: 1;}

            .dropdown:hover .dropdown-content {display: block;}
        </style>
    </head>
    <body>
        <h2>Hoverable Dropdown</h2>
        <p>Move the mouse over the text below to open the dropdown content.</p>

        <div class="dropdown">
            <span>Mouse over me</span>
            <div class="dropdown-content">
                <p>Hello World!</p>
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Dropdowns/Example_1.html)

## Dropdown menu

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .dropbtn {  background-color: #4CAF50;
                        color: white;
                        padding: 16px;
                        font-size: 16px;
                        border: none;
                        cursor: pointer;}

            .dropdown { position: relative;
                        display: inline-block;}

            .dropdown-content { display: none;
                                position: absolute;
                                background-color: #f9f9f9;
                                min-width: 160px;
                                box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
                                z-index: 1;}

            .dropdown-content a {   color: black;
                                    padding: 12px 16px;
                                    text-decoration: none;
                                    display: block;}

            .dropdown-content a:hover {background-color: #f1f1f1}

            .dropdown:hover .dropdown-content {display: block;}

            .dropdown:hover .dropbtn {background-color: #3e8e41;}
        </style>
    </head>
    <body>
        <h2>Dropdown Menu</h2>
        <p>Move the mouse over the button to open the dropdown menu.</p>

        <div class="dropdown">
            <button class="dropbtn">Dropdown</button>
            <div class="dropdown-content">
                <a href="#">Link 1</a>
                <a href="#">Link 2</a>
                <a href="#">Link 3</a>
            </div>
        </div>

        <p><strong>Note:</strong> We use href="#" for test links. In a real web site this would be URLs.</p>
    </body>
</html>
```

Output:

[Click here!](./Dropdowns/Example_2.html)

## Right-aligned dropdown menu

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .dropbtn {  background-color: #4CAF50;
                        color: white;
                        padding: 16px;
                        font-size: 16px;
                        border: none;
                        cursor: pointer;}

            .dropdown { position: relative;
                        display: inline-block;}

            .dropdown-content { display: none;
                                position: absolute;
                                right: 0;
                                background-color: #f9f9f9;
                                min-width: 160px;
                                box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
                                z-index: 1;}

            .dropdown-content a {   color: black;
                                    padding: 12px 16px;
                                    text-decoration: none;
                                    display: block;}

            .dropdown-content a:hover {background-color: #f1f1f1;}

            .dropdown:hover .dropdown-content {display: block;}

            .dropdown:hover .dropbtn {background-color: #3e8e41;}
        </style>
    </head>
    <body>
        <h2>Aligned Dropdown Content</h2>
        <p>Determine whether the dropdown content should go from left to right or right to left with the left and right properties.</p>

        <div class="dropdown" style="float:left;">
            <button class="dropbtn">Left</button>
            <div class="dropdown-content" style="left:0;">
                <a href="#">Link 1</a>
                <a href="#">Link 2</a>
                <a href="#">Link 3</a>
            </div>
        </div>

        <div class="dropdown" style="float:right;">
            <button class="dropbtn">Right</button>
            <div class="dropdown-content">
                <a href="#">Link 1</a>
                <a href="#">Link 2</a>
                <a href="#">Link 3</a>
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Dropdowns/Example_3.html)

## Dropdown image

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .dropdown { position: relative;
                        display: inline-block;}

            .dropdown-content { display: none;
                                position: absolute;
                                background-color: #f9f9f9;
                                min-width: 160px;
                                box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
                                z-index: 1;}

            .dropdown:hover .dropdown-content {display: block;}

            .desc { padding: 15px;
                    text-align: center;}
        </style>
    </head>
    <body>
        <h2>Dropdown Image</h2>
        <p>Move the mouse over the image below to open the dropdown content.</p>

        <div class="dropdown">
            <img src="../data/images/img_5terre.jpg" alt="Cinque Terre" width="100" height="50">
            <div class="dropdown-content">
                <img src="../data/images/img_5terre.jpg" alt="Cinque Terre" width="300" height="200">
                <div class="desc">Beautiful Cinque Terre</div>
            </div>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Dropdowns/Example_4.html)

## Dropdown navigation bar

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            body {background-color:white;}

            ul {list-style-type: none;
                margin: 0;
                padding: 0;
                overflow: hidden;
                background-color: #38444d;}

            li {float: left;}

            li a, .dropbtn {display: inline-block;
                            color: white;
                            text-align: center;
                            padding: 14px 16px;
                            text-decoration: none;}

            li a:hover, .dropdown:hover .dropbtn {background-color: red;}

            li.dropdown {display: inline-block;}

            .dropdown-content { display: none;
                                position: absolute;
                                background-color: #f9f9f9;
                                min-width: 160px;
                                box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
                                z-index: 1;}

            .dropdown-content a {   color: black;
                                    padding: 12px 16px;
                                    text-decoration: none;
                                    display: block;
                                    text-align: left;}

            .dropdown-content a:hover {background-color: #f1f1f1;}

            .dropdown:hover .dropdown-content {display: block;}
        </style>
    </head>
    <body>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#news">News</a></li>
            <li class="dropdown">
                <a href="javascript:void(0)" class="dropbtn">Dropdown</a>
                <div class="dropdown-content">
                    <a href="#">Link 1</a>
                    <a href="#">Link 2</a>
                    <a href="#">Link 3</a>
                </div>
            </li>
        </ul>

        <h3>Dropdown Menu inside a Navigation Bar</h3>
        <p>Hover over the "Dropdown" link to see the dropdown menu.</p>
    </body>
</html>
```

Output:

[Click here!](./Dropdowns/Example_5.html)