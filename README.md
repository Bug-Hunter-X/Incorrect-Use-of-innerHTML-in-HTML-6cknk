# Incorrect Use of innerHTML in HTML

This repository demonstrates a common, yet subtle error when using `innerHTML` in HTML to manipulate the DOM.  The incorrect usage can lead to unexpected behavior or even security vulnerabilities if not handled carefully.

## Bug Description

The `bug.html` file shows an example where `innerHTML` is used to append an entire `<p>` tag to an existing div. While functional in this simple case, directly using `innerHTML` with user-provided content can introduce XSS vulnerabilities.  It's also less efficient than using DOM manipulation methods.

## Solution

The `bugSolution.html` file provides the corrected approach. Instead of using `innerHTML`, it demonstrates how to create a new paragraph element (`<p>`) using `document.createElement('p')`, set its text content using `textContent`, and then append it to the parent div using `appendChild()`. This approach is safer and more efficient.

## How to reproduce the error

1. Open `bug.html` in a web browser.
2. Observe the output. While it appears correct, this is not the preferred way of adding new elements to the DOM.

## How to view the solution

1. Open `bugSolution.html` in a web browser.
2. Observe how the same outcome is achieved with a safer and more efficient method.