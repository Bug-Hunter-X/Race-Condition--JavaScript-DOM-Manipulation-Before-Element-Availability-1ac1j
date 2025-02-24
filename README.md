# Race Condition in HTML/JavaScript

This repository demonstrates a common yet often overlooked error in web development: attempting to manipulate a DOM element via JavaScript before the element has been fully parsed and rendered by the browser.  This can lead to unexpected behavior or errors.

## The Bug

The `bug.html` file contains a simple HTML page with a div element. A JavaScript script attempts to modify the display style of the div. However, the script executes *before* the browser has finished rendering the div, leading to an error (in some browsers) or simply no effect (in others).

## The Solution

The `solution.html` file corrects this issue by using the `DOMContentLoaded` event.  This event ensures the script only runs once the entire HTML document is loaded and the DOM is ready for manipulation.  This prevents the race condition.