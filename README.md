# Uncommon HTML Bug: Incorrect innerHTML Usage with <script> Tag

This repository demonstrates an uncommon bug related to the use of `innerHTML` in HTML to insert a `<script>` tag.  Improperly using `innerHTML` to add scripts can lead to unexpected behavior and security vulnerabilities, primarily cross-site scripting (XSS). 

The `bug.html` file shows the problematic code. The solution is demonstrated in `bugSolution.html`.

## Bug Description

Using `innerHTML` to dynamically add `<script>` tags is generally discouraged.  This approach can introduce security risks and lead to unpredictable results if not handled carefully. It can also cause issues if the added script tries to interact with existing JavaScript code in unpredictable ways.

## Solution

Instead of using `innerHTML`, it's recommended to create a new `<script>` element and append it to the DOM using the `appendChild` method.  This offers better control over the script's execution context and is safer.