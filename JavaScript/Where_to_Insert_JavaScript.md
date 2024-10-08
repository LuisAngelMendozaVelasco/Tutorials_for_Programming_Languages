# Where to Insert JavaScript

## JavaScript in `<head>`

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <script>
            function myFunction() {
                document.getElementById("demo").innerHTML = "Paragraph changed.";
            }
        </script>
    </head>
    <body>
        <h2>Demo JavaScript in Head</h2>

        <p id="demo">A Paragraph.</p>

        <button type="button" onclick="myFunction()">Try it</button>
    </body>
</html> 
```

Output:

[Click here!](./Where_to_Insert_JavaScript/Example_1.html)

## JavaScript in `<body>`

Code: 

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Demo JavaScript in Body</h2>

        <p id="demo">A Paragraph.</p>

        <button type="button" onclick="myFunction()">Try it</button>

        <script>
            function myFunction() {
                document.getElementById("demo").innerHTML = "Paragraph changed.";
            }
        </script>
    </body>
</html> 
```

Output:

[Click here!](./Where_to_Insert_JavaScript/Example_2.html)

## JavaScript in an external file

Code: 

```js
function myFunction() {
    document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Demo External JavaScript</h2>

        <p id="demo">A Paragraph.</p>

        <button type="button" onclick="myFunction()">Try it</button>

        <p>This example links to "myScript.js".</p>
        <p>(myFunction is stored in "myScript.js")</p>

        <script src="./myScript.js"></script>
    </body>
</html>
```

Output:

[Click here!](./Where_to_Insert_JavaScript/Example_3.html)

## JavaScript in an external url

Code: 

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>External JavaScript</h2>

        <p id="demo">A Paragraph.</p>

        <button type="button" onclick="myFunction()">Click Me</button>

        <p>This example uses a full web URL to link to "myScript.js".</p>
        <p>(myFunction is stored in "myScript.js")</p>

        <script src="https://www.w3schools.com/js/myScript.js"></script>
    </body>
</html>
```

Output:

[Click here!](./Where_to_Insert_JavaScript/Example_4.html)

## JavaScript in an external folder

```js
function myFunction() {
    document.getElementById("demo").innerHTML = "Paragraph changed.";
}
```

Code: 

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>External JavaScript</h2>

        <p id="demo">A Paragraph.</p>

        <button type="button" onclick="myFunction()">Try it</button>

        <p>This example uses a file path to link to "myScript.js".</p>
        <p>(myFunction is stored in "myScript.js")</p>

        <script src="./js/myScript.js"></script>
    </body>
</html>
```

Output:

[Click here!](./Where_to_Insert_JavaScript/Example_5.html)