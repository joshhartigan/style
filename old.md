# Multi-Language Style Guide
*A guide to consistent style in program source code of different languages, inspired by [airbnb/javascript](https://github.com/airbnb/javascript)*
(Not all my code uses this, but all code written in the future will, and I will work on cleaning up past code).

## Table of Contents
1. [Indentation](#indentation)
1. [Braces](#braces)
1. [Comments](#comments)
1. [Naming Things](#naming-things)
1. [Whitespace](#whitespace)
1. [Strings](#strings)
1. [Editors](#editors)

## Indentation
- Soft tabs, 2 spaces
  - Except for Python - soft tabs, 4 spaces)
  - Except for Golang - hard tabs, 8 spaces (use `gofmt`)

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

- Do not indent `case` lines in switch statements:

```cpp
// wrong
switch (age) {
  case 20:
  return true;
  case 80:
  return false;
  default:
  return true;
}

// right
switch (age) {
case 20:
  return true;
case 80:
  return false;
default:
  return true;
}
```

- In long method calls, use indentation following this rule / common sense:

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
- Always use braces with if statements and loops. This is because if and when
  a time comes at which you need to add lines in an if statement, you won't make
  the mistake of not including braces:

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

- Opening braces never have a line to themselves:

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
- Multiline comments over 5 lines follow `/** comment */` syntax:

```java
// wrong
// Set the fur thickness for a Squirrel object.
// Parameter: thickness (int)
// TODO: Implement RedSquirrel support
// TODO: Create support for all animals with fur
//       (will require a 'FurryAnimal' class)
void setThickness (int thickness) {
  this.thickness = thickness;
}

// right
/**
 * Set the fur thickness for a Squirrel object.
 * Parameter: thickness (int)
 * TODO: Implement RedSquirrel support
 * TODO: Create support for all animals with fur
 *       (will require a 'FurryAnimal' class)
 */
 void setThickness (int thickness) {
  this.thickness = thickness;
}
```

- The body of a single-line comment should always begin with a space:

```java
//wrong
// right
```

**[⬆ back to top](#table-of-contents)**

## Naming Things

- Follow these naming guidelines, unless another rule says otherwise:

```cpp
// All languages:
int CONSTANT_VARIABLE;
class ClassName;
void functionName;
char localVariable;

```
```java
// java package names:

// wrong
com.company.packageName;

// right
com.company.packagename;
```

* In languages that don't require a certain file name:

```
program_name.x
// or
program-name.x
```

- These rules can be bypassed if they need to be (for example, in Go, where exported names begin with a capital letter).

- Capitalised acronyms/initialisms, such as HTML and HTTP, should only keep their first capital:

```
// wrong
HTTPHTMLRequest request;

// right
HttpHtmlRequest request;
```

- Avoid shortened names, unless they're scarce (such as in a for loop, or used once in an if statement/chain):

```go
// wrong
MonsterDungeon m;

// right
MonsterDungeon firstDungeon;

// allowed:
for i := 0; i < 10; i++ { }

// allowed:
if r := math.Sqrt(inputNumber); r < 250 { }
```
- Similarly, avoid lengthy names that can be reduced in length:

```python
# wrong
nameOfRoomThatPlayerIsCurrentlyIn = "Haunted Mansion"
# right
currentRoom = "Haunted Mansion"
```

- Name variables that are opposites precisely, and consistently:

```javascript
// wrong
contestant.next();
contestant.back();

// right
contestant.next();
contestant.previous();
```

- **JavaScript**: Always use the `var` keyword, to keep the global namespace clean:

```javascript
// wrong
userName = "Eddard";

// right
var userName = "Eddard";

// also right for multiple variables, if indented as such:
var userName = "Eddard",
  userAge = 42,
  userColour = colors.BLUE;
```

**[⬆ back to top](#table-of-contents)**


## Whitespace

*This section does not deal with [indentation](#indentation).*

- Always surround operators with a single space, except for increment/decrement operators (++ and --):

```javascript
// wrong
4+4;
myName="Josh";
for (var i=0; i<length; i ++) { }

// right
4 + 4;
myName = "Josh";
for (var i = 0; i < length; i++) { }
```

- End every file with a single blank line - this is POSIX standard.
  Vim will do this for you.

- In a parenthesised for, if, while, etc. statement, insert spaces before and after the parentheses:

```cpp
// wrong
if(age > 18){
  // ...
}

// right
if (age > 18) {
  // ...
}
```

- In function calls or container[item] identifiers that contain other function
  calls or container[item], wrap the inside of the parentheses or square
  brackets in a space:

```javascript
doFunction( getAgeOfPanda() + 4 );
endangeredPandas[ nthPanda() + 1 ];
```

**[⬆ back to top](#table-of-contents)**

## Strings

- Use double quotes or single quotes, but keep it consistent:

```python
# wrong
def main():
  print 'hello, world'
  print "he said hello"

# right
def main():
  print "hello, world"
  print "he said \"hello\""
```

- **Strict**: In Ruby, use single quotes, but use double quotes for string interpolation.

**[⬆ back to top](#table-of-contents)**

## Editors

- Use the [only true editor](http://www.vim.org).

**[⬆ back to top](#table-of-contents)**
