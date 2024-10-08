# Variables

## Using the var() function

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            :root { --blue: #1e90ff;
                    --white: #ffffff;}

            body {background-color: var(--blue);}

            h2 {border-bottom: 2px solid var(--blue);}

            .container {color: var(--blue);
                        background-color: var(--white);
                        padding: 15px;}

            button {background-color: var(--white);
                    color: var(--blue);
                    border: 1px solid var(--blue);
                    padding: 5px;}
        </style>
    </head>
    <body>
        <h1>Using the var() Function</h1>

        <div class="container">
            <h2>Lorem Ipsum</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit.</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit.</p>
            <p>
                <button>Yes</button>
                <button>No</button>
            </p>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Variables/Example_1.html)

## Using the var() function to insert several custom property values

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            :root { --blue: #6495ed;
                    --white: #faf0e6;}

            body {background-color: var(--blue);}

            h2 {border-bottom: 2px solid var(--blue);}

            .container {color: var(--blue);
                        background-color: var(--white);
                        padding: 15px;}

            button {background-color: var(--white);
                    color: var(--blue);
                    border: 1px solid var(--blue);
                    padding: 5px;}
        </style>
    </head>
    <body>
        <h1>Using the var() Function</h1>

        <div class="container">
            <h2>Lorem Ipsum</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit.</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam semper diam at erat pulvinar, at pulvinar felis blandit.</p>
            <p>
                <button>Yes</button>
                <button>No</button>
            </p>
        </div>
    </body>
</html>
```

Output:

[Click here!](./Variables/Example_2.html)