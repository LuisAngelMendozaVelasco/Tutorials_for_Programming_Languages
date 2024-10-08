# Geolocation

## Get geolocation coordinates

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>Click the button to get your coordinates.</p>

        <button onclick="getLocation()">Try It</button>

        <p id="demo"></p>

        <script>
            var x = document.getElementById("demo");

            function getLocation() {
                if (navigator.geolocation) {
                    navigator.geolocation.getCurrentPosition(showPosition);
                } 
                else { 
                    x.innerHTML = "Geolocation is not supported by this browser.";
                }
            }

            function showPosition(position) {
                x.innerHTML = "Latitude: " + position.coords.latitude + "<br>Longitude: " + position.coords.longitude;
            }
        </script>
    </body>
</html>
```

Output:

[Click here!](./Geolocation/Example_1.html)

## Handle geolocation errors

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>Click the button to get your coordinates.</p>

        <button onclick="getLocation()">Try It</button>

        <p id="demo"></p>

        <script>
            var x = document.getElementById("demo");

            function getLocation() {
                if (navigator.geolocation) {
                    navigator.geolocation.getCurrentPosition(showPosition, showError);
                } 
                else { 
                    x.innerHTML = "Geolocation is not supported by this browser.";
                }
            }

            function showPosition(position) {
                x.innerHTML = "Latitude: " + position.coords.latitude + "<br>Longitude: " + position.coords.longitude;
            }

            function showError(error) {
                switch(error.code) {
                    case error.PERMISSION_DENIED:
                        x.innerHTML = "User denied the request for Geolocation."
                        break;
                    case error.POSITION_UNAVAILABLE:
                        x.innerHTML = "Location information is unavailable."
                        break;
                    case error.TIMEOUT:
                        x.innerHTML = "The request to get user location timed out."
                        break;
                    case error.UNKNOWN_ERROR:
                        x.innerHTML = "An unknown error occurred."
                        break;
                }
            }
        </script>
    </body>
</html>
```

Output:

[Click here!](./Geolocation/Example_2.html)

## Get geolocation and watch the position

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>Click the button to get your coordinates.</p>

        <button onclick="getLocation()">Try It</button>

        <p id="demo"></p>

        <script>
            var x = document.getElementById("demo");

            function getLocation() {
                if (navigator.geolocation) {
                    navigator.geolocation.watchPosition(showPosition);
                } 
                else { 
                    x.innerHTML = "Geolocation is not supported by this browser.";
                }
            }
                
            function showPosition(position) {
                x.innerHTML = "Latitude: " + position.coords.latitude + "<br>Longitude: " + position.coords.longitude;
            }
        </script>
    </body>
</html>
```

Output:

[Click here!](./Geolocation/Example_3.html)