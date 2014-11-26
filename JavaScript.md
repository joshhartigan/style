# JavaScript Style Guide

#### Semicolons

* Only use semicolons for multiple statements in one line.
  However, multiple statements in one line should be avoided
  outside of for loop headers.

#### Variables

* Always use `var`.

* Follow naming syntax as follows:

  ```javascript
  var normalVariable = 2
  var CONSTANT_VARIABLE = 'africa'
  ```

* Single-char variable names are only acceptable for
  one-time equations, positioning variables (e.g. `x` and `y`),
  and for loops (use `i`, `j`, `k`, `l`, etc.)


#### Comments

* Use double slashes `//` unless the comment is over 5 lines,
  in which case follow this syntax:

  ```javascript
  /**
   * This is a long comment that
   * explains the functionality
   * of a thing that is created
   * to manage and manipulate
   * things that create other
   * things that do when can
   * they not.
   */
 ```

* Comments explain *why*, code expalins *what*.


#### Parentheses

* Follow the rules that are demonstrated below in regards to
  parentheses:

  ```javascript
  function blahBlah() {
    // ...
  }

  // space before opener in loops and if/else/switch statements
  if (x && y) {
    // ...
  }

  // parentheses are padded with spaces if there
  // are more parentheses inside it
  blahBlah( function(x) { return x } )

  if ( isNaN(x) ) {
    // ...
  }
  ```

