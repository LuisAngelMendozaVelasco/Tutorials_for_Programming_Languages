# Web Fonts

## Use your "own" fonts in @font-face rule

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style> 
            @font-face {font-family: myFirstFont;
                        src: url(../data/fonts/sansation_light.woff);}

            * {font-family: myFirstFont;}
        </style>
    </head>
    <body>
        <h1>The @font-face Rule</h1>

        <div>
            With CSS, websites can use fonts other than the pre-selected "web-safe" fonts.
        </div>
    </body>
</html>
```

Output:

[Click here!](./Web_Fonts/Example_1.html)

## Use your "own" fonts in @font-face rule (bold)

Code: 

```html
<!DOCTYPE html>
<html>
    <head>
        <style> 
            @font-face {font-family: myFirstFont;
                        src: url(../data/fonts/sansation_light.woff);}

            @font-face {font-family: myFirstFont;
                        src: url(../data/fonts/sansation_bold.woff);
                        font-weight: bold;}

            * {font-family: myFirstFont;}
        </style>
    </head>
    <body>
        <h1>The @font-face Rule</h1>

        <div>
            With CSS, websites can use <b>fonts other than the pre-selected "web-safe" fonts</b>.
        </div>
    </body>
</html>
```

Output:

[Click here!](./Web_Fonts/Example_2.html)