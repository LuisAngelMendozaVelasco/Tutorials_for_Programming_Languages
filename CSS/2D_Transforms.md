# 2D Transforms

## translate() - move an element from its current position

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style> 
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;
                    transform: translate(50px, 100px);}
        </style>
    </head>
    <body>
        <h1>The translate() Method</h1>
        <p>The translate() method moves an element from its current position:</p>

        <div>
            This div element is moved 50 pixels to the right, and 100 pixels down from its current position.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_1.html)

## rotate() - rotate an element clockwise

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;}

            div#myDiv {transform: rotate(20deg);}
        </style>
    </head>
    <body>
        <h1>The rotate() Method</h1>

        <p>The rotate() method rotates an element clockwise or counter-clockwise.</p>

        <div>
            This a normal div element.
        </div>

        <div id="myDiv">
            This div element is rotated clockwise 20 degrees.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_2.html)

## rotate() - rotate an element counter-clockwise

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;}

            div#myDiv {transform: rotate(-20deg);}
        </style>
    </head>
    <body>
        <h1>The rotate() Method</h1>

        <p>The rotate() method rotates an element clockwise or counter-clockwise.</p>

        <div>
            This a normal div element.
        </div>

        <div id="myDiv">
            This div element is rotated counter-clockwise with 20 degrees.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_3.html)

## scale() - increase an element

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   margin: 150px;
                    width: 200px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;
                    transform: scale(2, 3);}
        </style>
    </head>
    <body>
        <h1>The scale() Method</h1>

        <p>The scale() method increases or decreases the size of an element.</p>

        <div>
            This div element is two times of its original width, and three times of its original height.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_4.html)

## scale() - decrease an element

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   margin: 150px;
                    width: 200px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;
                    transform: scale(0.5, 0.5);}
        </style>
    </head>
    <body>
        <h1>The scale() Method</h1>

        <p>The scale() method increases or decreases the size of an element.</p>

        <div>
            This div element is decreased to be half of its original width and height.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_5.html)

## skewX() - skews an element along the X-axis

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;}

            div#myDiv {transform: skewX(20deg);}
        </style>
    </head>
    <body>
        <h1>The skewX() Method</h1>

        <p>The skewX() method skews an element along the X-axis by the given angle.</p>

        <div>
            This a normal div element.
        </div>

        <div id="myDiv">
            This div element is skewed 20 degrees along the X-axis.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_6.html)

## skewY() - skews an element along the Y-axis

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;}

            div#myDiv {transform: skewY(20deg);}
        </style>
    </head>
    <body>
        <h1>The skewY() Method</h1>

        <p>The skewY() method skews an element along the Y-axis by the given angle.</p>

        <div>
            This a normal div element.
        </div>

        <div id="myDiv">
            This div element is skewed 20 degrees along the Y-axis.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_7.html)

## skew() - skews an element along the X and Y-axis

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;}

            div#myDiv {transform: skew(20deg, 10deg);}
        </style>
    </head>
    <body>
        <h1>The skew() Method</h1>
        <p>The skew() method skews an element into a given angle.</p>

        <div>
            This a normal div element.
        </div>

        <div id="myDiv">
            This div element is skewed 20 degrees along the X-axis, and 10 degrees along the Y-axis.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_8.html)

## matrix() - rotate, scale, move, and skew an element

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            div {   width: 300px;
                    height: 100px;
                    background-color: yellow;
                    border: 1px solid black;}

            div#myDiv1 {transform: matrix(1, -0.3, 0, 1, 0, 0);}

            div#myDiv2 {transform: matrix(1, 0, 0.5, 1, 150, 0);}
        </style>
    </head>
    <body>
        <h1>The matrix() Method</h1>

        <p>The matrix() method combines all the 2D transform methods into one.</p>

        <div>
            This a normal div element.
        </div>

        <div id="myDiv1">
            Using the matrix() method.
        </div>

        <div id="myDiv2">
            Another use of the matrix() method.
        </div>
    </body>
</html>
```

Output:

[Click here!](./2D_Transforms/Example_9.html)