# Uncommon HTML Error: Accessing Non-Existent Attributes

This repository demonstrates a subtle error that can occur in HTML when attempting to access attributes that might not exist on an element.  While not a syntax error, it can lead to unexpected behavior and potential bugs in larger applications.

## Description

The `bug.html` file contains a simple HTML structure with a div element.  A JavaScript snippet attempts to access a non-existent attribute ("nonExistentAttr") using the `getAttribute()` method.  While this doesn't throw an error directly, it returns `null`, which might not be the expected behavior and could have unintended consequences in more complex scenarios.

## Solution

The `bugSolution.html` file offers a more robust solution. Before attempting to access the attribute, it checks for its existence using `hasAttribute()`.  This avoids attempting to access a potentially null value and prevents unexpected errors.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.  Observe the console; it should log 'null'.
3. Open `bugSolution.html`. The console will demonstrate a robust way to handle attribute access without errors.