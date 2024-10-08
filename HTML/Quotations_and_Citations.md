# Quotations and Citations

## Formatting short quotations with the `<q>` element

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>Browsers usually insert quotation marks around the q element.</p>
        <p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
    </body>
</html>
```

Output:

[Click here!](./Quotations_and_Citations/Example_1.html)

## Formatting quoted sections with the `<blockquote>` element

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>Here is a quote from WWF's website:</p>
        <blockquote cite="http://www.worldwildlife.org/who/index.html">
            For 60 years, WWF has worked to help people and nature thrive. As the world's leading conservation organization, WWF works in nearly 100 countries. At every level, we collaborate with people around the world to develop and deliver innovative solutions that protect communities, wildlife, and the places in which they live.
        </blockquote>
    </body>
</html>
```

Output:

[Click here!](./Quotations_and_Citations/Example_2.html)

## Formatting document author/owner information with the `<address>` element

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>The HTML address element defines contact information (author/owner) of a document or article.</p>
        <address>
            Written by John Doe.<br> 
            Visit us at:<br>
            Example.com<br>
            Box 564, Disneyland<br>
            USA
        </address>
    </body>
</html>
```

Output:

[Click here!](./Quotations_and_Citations/Example_3.html)

## Formatting abbreviations and acronyms the `<abbr>` element

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
        <p>Marking up abbreviations can give useful information to browsers, translation systems and search-engines.</p>
    </body>
</html>
```

Output:

[Click here!](./Quotations_and_Citations/Example_4.html)

## Formatting work title with the `<cite>` element

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>The HTML cite element defines the title of a work.</p>
        <p>Browsers usually display cite elements in italic.</p>
        <img src="../data/images/img_the_scream.jpg" width="220" height="277" alt="The Scream">
        <p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
    </body>
</html>
```

Output:

[Click here!](./Quotations_and_Citations/Example_5.html)

## Formatting text direction with the `<bdo>` element

Code:

```html
<!DOCTYPE html>
<html>
    <body>
        <p>If your browser supports bi-directional override (bdo), the next line will be written from right to left (rtl):</p>
        <bdo dir="rtl">This line will be written from right to left</bdo>
    </body>
</html>
```

Output:

[Click here!](./Quotations_and_Citations/Example_6.html)