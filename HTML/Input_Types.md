# Input Types

## Input type text

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Text field</h2>
        <p>The <strong>input type="text"</strong> defines a one-line text input field:</p>

        <form action="/action_page.php">
            <label for="fname">First name:</label><br>
            <input type="text" id="fname" name="fname"><br>
            <label for="lname">Last name:</label><br>
            <input type="text" id="lname" name="lname"><br><br>
            <input type="submit" value="Submit">
        </form>

        <p>Note that the form itself is not visible.</p>
        <p>Also note that the default width of a text field is 20 characters.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_1.html)

## Input type password

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Password field</h2>

        <p>The <strong>input type="password"</strong> defines a password field:</p>

        <form action="/action_page.php">
            <label for="username">Username:</label><br>
            <input type="text" id="username" name="username"><br>
            <label for="pwd">Password:</label><br>
            <input type="password" id="pwd" name="pwd"><br><br>
            <input type="submit" value="Submit">
        </form>

        <p>The characters in a password field are masked (shown as asterisks or circles).</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_2.html)

## Input type radio

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Radio Buttons</h2>

        <p>The <strong>input type="radio"</strong> defines a radio button:</p>

        <p>Choose your favorite Web language:</p>
        <form action="/action_page.php">
            <input type="radio" id="html" name="fav_language" value="HTML">
            <label for="html">HTML</label><br>
            <input type="radio" id="css" name="fav_language" value="CSS">
            <label for="css">CSS</label><br>
            <input type="radio" id="javascript" name="fav_language" value="JavaScript">
            <label for="javascript">JavaScript</label><br><br>
            <input type="submit" value="Submit">
        </form> 
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_3.html)

## Input type checkbox

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Checkboxes</h2>
        <p>The <strong>input type="checkbox"</strong> defines a checkbox:</p>

        <form action="/action_page.php">
            <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
            <label for="vehicle1"> I have a bike</label><br>
            <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
            <label for="vehicle2"> I have a car</label><br>
            <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
            <label for="vehicle3"> I have a boat</label><br><br>
            <input type="submit" value="Submit">
        </form> 
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_4.html)

## Input type button

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Input Button</h2>

        <input type="button" onclick="alert('Hello World!')" value="Click Me!">
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_5.html)

## Input type number with restrictions

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Number Field</h2>

        <p>The <strong>input type="number"</strong> defines a numeric input field.</p>

        <p>You can use the min and max attributes to add numeric restrictions in the input field:</p>

        <form action="/action_page.php">
            <label for="quantity">Quantity (between 1 and 5):</label>
            <input type="number" id="quantity" name="quantity" min="1" max="5">
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_6.html)

## Input type number with steps

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Numeric Steps</h2>

        <p>Depending on browser support: Fixed steps will apply in the input field.</p>

        <form action="/action_page.php">
            <label for="quantity">Quantity:</label>
            <input type="number" id="quantity" name="quantity" min="0" max="100" step="10" value="30">
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_7.html)

## Input type date with date picker

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Date Field</h2>

        <p>The <strong>input type="date"</strong> is used for input fields that should contain a date.</p>

        <form action="/action_page.php">
            <label for="birthday">Birthday:</label>
            <input type="date" id="birthday" name="birthday">
            <input type="submit" value="Submit">
        </form>

        <p><strong>Note:</strong> type="date" is not supported in Internet Explorer 11 or prior Safari 14.1.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_8.html)

## Input type date with restrictions

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Date Field Restrictions</h2>

        <p>Use the min and max attributes to add restrictions to dates:</p>

        <form action="/action_page.php">
            <label for="datemin">Enter a date after 2000-01-01:</label>
            <input type="date" id="datemin" name="datemin" min="2000-01-02"><br><br>

            <label for="datemax">Enter a date before 1980-01-01:</label>
            <input type="date" id="datemax" name="datemax" max="1979-12-31"><br><br>
            
            <input type="submit" value="Submit">
        </form>

        <p><strong>Note:</strong> type="date" is not supported in Internet Explorer 11 or prior Safari 14.1.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_9.html)

## Input type color with color picker

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Show a Color Picker</h2>

        <p>The <strong>input type="color"</strong> is used for input fields that should contain a color.</p>

        <form action="/action_page.php">
            <label for="favcolor">Select your favorite color:</label>
            <input type="color" id="favcolor" name="favcolor" value="#ff0000">
            <input type="submit" value="Submit">
        </form>

        <p><b>Note:</b> type="color" is not supported in Internet Explorer 11 or Safari 9.1 (or earlier).</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_10.html)

## Input type range

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Range Field</h2>

        <p>Depending on browser support: The input type "range" can be displayed as a slider control.</p>

        <form action="/action_page.php" method="get">
            <label for="vol">Volume (between 0 and 50):</label>
            <input type="range" id="vol" name="vol" min="0" max="50">
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_11.html)

## Input type month

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Month Field</h2>

        <p>The <strong>input type="month"</strong> allows the user to select a month and year.</p>

        <form action="/action_page.php">
            <label for="bdaymonth">Birthday (month and year):</label>
            <input type="month" id="bdaymonth" name="bdaymonth">
            <input type="submit" value="Submit">
        </form>

        <p><strong>Note:</strong> type="month" is not supported in Firefox, Safari, or Internet Explorer 11.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_12.html)

## Input type week

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h1>Display a Week Input Control</h1>

        <p>The <strong>input type="week"</strong> allows the user to select a week and year.</p>

        <p>If the browser supports it, a date picker pops up when entering the input field.</p>

        <form action="/action_page.php">
            <label for="week">Select a week:</label>
            <input type="week" id="week" name="week">
            <input type="submit" value="Submit">
        </form>

        <p><strong>Note:</strong> type="week" is not supported in Firefox, Safari or Internet Explorer 11.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_13.html)

## Input type time

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h1>Show a Time Input Control</h1>

        <p>The <strong>input type="time"</strong> allows the user to select a time (no time zone):</p>

        <p>If the browser supports it, a time picker pops up when entering the input field.</p>

        <form action="/action_page.php">
            <label for="appt">Select a time:</label>
            <input type="time" id="appt" name="appt">
            <input type="submit" value="Submit">
        </form>

        <p><strong>Note:</strong> type="time" is not supported in Internet Explorer 11 or prior Safari 14.1.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_14.html)

## Input type datetime-local

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Local Date Field</h2>

        <p>The <strong>input type="datetime-local"</strong> specifies a date and time input field, with no time zone.</p>

        <form action="/action_page.php">
            <label for="birthdaytime">Birthday (date and time):</label>
            <input type="datetime-local" id="birthdaytime" name="birthdaytime">
            <input type="submit" value="Submit">
        </form>

        <p><strong>Note:</strong> type="datetime-local" is not supported in Internet Explorer 11 or prior Safari 14.1.</p>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_16.html)

## Input type email

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Email Field</h2>

        <p>The <strong>input type="email"</strong> is used for input fields that should contain an e-mail address:</p>

        <form action="/action_page.php">
            <label for="email">Enter your email:</label>
            <input type="email" id="email" name="email">
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_17.html)

## Input type search

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Search Field</h2>
        <p>The <strong>input type="search"</strong> is used for search fields (behaves like a regular text field):</p>

        <form action="/action_page.php">
            <label for="gsearch">Search Google:</label>
            <input type="search" id="gsearch" name="gsearch">
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_18.html)

## Input type tel

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h2>Telephone Field</h2>

        <p>The <strong>input type="tel"</strong> is used for input fields that should contain a telephone number:</p>

        <form action="/action_page.php">
            <label for="phone">Enter a phone number:</label><br><br>
            <input type="tel" id="phone" name="phone" placeholder="123-45-678" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" required><br><br>
            <small>Format: 123-45-678</small><br><br>
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_19.html)

## Input type url

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <h1>Display a URL Input Field</h1>

        <p>The <strong>input type="url"</strong> is used for input fields that should contain a URL address:</p>

        <form action="/action_page.php">
            <label for="homepage">Add your homepage:</label>
            <input type="url" id="homepage" name="homepage">
            <input type="submit" value="Submit">
        </form>
    </body>
</html>
```

Output:

[Click here!](./Input_Types/Example_20.html)