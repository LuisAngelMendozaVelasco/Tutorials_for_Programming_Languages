# Local Storage

## Store a name permanently

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <div id="result"></div>

        <script>
            // Check browser support
            if (typeof(Storage) !== "undefined") {
                // Store
                localStorage.setItem("lastname", "Smith");
                // Retrieve
                document.getElementById("result").innerHTML = localStorage.getItem("lastname");
            } 
            else {
                document.getElementById("result").innerHTML = "Sorry, your browser does not support Web Storage...";
            }
        </script>
    </body>
</html>
```

Output:

[Click here!](./Local_Storage/Example_1.html)

## Store a counter permanently

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <script>
            function clickCounter() {
                if (typeof(Storage) !== "undefined") {
                    if (localStorage.clickcount) {
                        localStorage.clickcount = Number(localStorage.clickcount) + 1;
                    } 
                    else {
                        localStorage.clickcount = 1;
                    }
                    document.getElementById("result").innerHTML = "You have clicked the button " + localStorage.clickcount + " time(s).";
                } 
                else {
                    document.getElementById("result").innerHTML = "Sorry, your browser does not support web storage...";
                }
            }
        </script>
    </head>
    <body>
        <p><button onclick="clickCounter()" type="button">Click me!</button></p>
        <div id="result"></div>
        <p>Click the button to see the counter increase.</p>
        <p>Close the browser tab (or window), and try again, and the counter will continue to count (is not reset).</p>
    </body>
</html>
```

Output:

[Click here!](./Local_Storage/Example_2.html)

## Store a counter for one session

Code:

```html
<!DOCTYPE html>
<html>
    <head>
        <script>
            function clickCounter() {
                if (typeof(Storage) !== "undefined") {
                    if (sessionStorage.clickcount) {
                        sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
                    } 
                    else {
                        sessionStorage.clickcount = 1;
                    }
                    document.getElementById("result").innerHTML = "You have clicked the button " + sessionStorage.clickcount + " time(s) in this session.";
                } 
                else {
                    document.getElementById("result").innerHTML = "Sorry, your browser does not support web storage...";
                }
            }
        </script>
    </head>
    <body>
        <p><button onclick="clickCounter()" type="button">Click me!</button></p>
        <div id="result"></div>
        <p>Click the button to see the counter increase.</p>
        <p>Close the browser tab (or window), and try again, and the counter is reset.</p>
    </body>
</html>
```

Output:

[Click here!](./Local_Storage/Example_3.html)