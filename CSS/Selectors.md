# Selectors

## The element selector

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p { text-align: center;
                color: red;} 
        </style>
    </head>
    <body>
        <p>Every paragraph will be affected by the style.</p>
        <p id="para1">Me too!</p>
        <p>And me!</p>
    </body>
</html>
```

Output:

[Click here!](./Selectors/Example_1.html)

## The id selector

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            #para1 {text-align: center;
                    color: red;}
        </style>
    </head>
    <body>
        <p id="para1">Hello World!</p>
        <p>This paragraph is not affected by the style.</p>
    </body>
</html>
```

Output:

[Click here!](./Selectors/Example_2.html)

## The class selector (for all elements)

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .center {   text-align: center;
                        color: red;}
        </style>
    </head>
    <body>
        <h1 class="center">Red and center-aligned heading</h1>
        <p class="center">Red and center-aligned paragraph.</p> 
    </body>
</html>
```

Output:

[Click here!](./Selectors/Example_3.html)

## The class selector (for only `<p>` elements)

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p.center {  text-align: center;
                        color: red;}
        </style>
    </head>
    <body>
        <h1 class="center">This heading will not be affected</h1>
        <p class="center">This paragraph will be red and center-aligned.</p> 
    </body>
</html>   
```

Output:

[Click here!](./Selectors/Example_4.html)

## An HTML element that refer to two classes

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            p.center {  text-align: center;
                        color: red;}

            p.large {font-size: 300%;}
        </style>
    </head>
    <body>
        <h1 class="center">This heading will not be affected</h1>
        <p class="center">This paragraph will be red and center-aligned.</p>
        <p class="center large">This paragraph will be red, center-aligned, and in a large font-size.</p> 
    </body>
</html>
```

Output:

[Click here!](./Selectors/Example_5.html)

## The universal selector

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            * { text-align: center;
                color: blue;}
        </style>
    </head>
    <body>
        <h1>Hello world!</h1>
        <p>Every element on the page will be affected by the style.</p>
        <p id="para1">Me too!</p>
        <p>And me!</p>
    </body>
</html>
```

Output:

[Click here!](./Selectors/Example_6.html)

## Grouping selectors

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            h1, h2, p { text-align: center;
                        color: red;}
        </style>
    </head>
    <body>
        <h1>Hello World!</h1>
        <h2>Smaller heading!</h2>
        <p>This is a paragraph.</p>
    </body>
</html>
```

Output:

[Click here!](./Selectors/Example_7.html)