# Multi-Language Style Guide
*A guide to consistent style in program source code of different languages, inspired by [airbnb/javascript](https://github.com/airbnb/javascript)*
(Not all my code uses this, but all code written in the future will, and I will work on cleaning up past code).

## Table of Contents
1. [Indentation](#indentation)
1. [Braces](#braces)
1. [Comments](#comments)

## Indentation
- Soft tabs, 2 spaces (except for Python - soft tabs, 4 spaces)

```javascript
// wrong
if (name == "John") {
∙∙∙∙greetUser();
}

// wrong
if (name == "John") {
\tgreetUser(); // (using tab)
}

// right
if (name == "John") {
∙∙greetUser();
}
```

- **C++**: Do not indent `public`, `private`, or `protected` accessors:

```cpp
// wrong
class Awesome {
∙∙public:
∙∙∙∙int publicVariable;
∙∙private:
∙∙∙∙int privateVariable;
};

// right
class Awesome {
public:
∙∙int publicVariable;
private:
∙∙int privateVariable;
};
```

- In long method calls, use indentation following this rule:

```javascript
// wrong
$("element").find(".aClass").action().end().find(".otherClass").otherAction().end()

// right
$("element")
  .find(".aClass")
    .action()
    .end()
  .find(".otherClass")
    .otherAction()
    .end()
```

**[⬆ back to top](#table-of-contents)**

## Braces
- Always use braces with if statements and loops:

```java
// wrong
if (completed)
	finishGame();

// right
if (completed) {
	finishGame();
}
```

- Put a space before each semicolon:

```cpp
// bad
class Base{
	// ...
}

// good
class Base {
	// ...
}
```

- Braces never have a line to themselves:

```javascript
// wrong
function()
{
	alert("hi");
}

// right
function() {
	alert("hi");
}
```

**[⬆ back to top](#table-of-contents)**

## Comments

- Multiline comments follow `/** comment */` syntax:

```java
// wrong
// Set the fur thickness for a Squirrel object.
// Parameter: thickness (int)
void setThickness (int thickness) {
	this.thickness = thickness;
}

// right
/**
 * Set the fur thickness for a Squirrel object.
 * @param {int} thickness
 */
void setThickness (int thickness) {
	this.thickness = thickness;
}
```

**[⬆ back to top](#table-of-contents)**
