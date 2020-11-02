# JavaScript coding conventions
## -style guide-

* functions: lowerUpper()
- It's a best practice to actually tell what the function is doing by giving the function name a verb as prefix:
```
  // bad
  function name(firstName, lastName) {
    return `${firstName} ${lastName}`;
  }

  // good
  function getName(firstName, lastName) {
    return `${firstName} ${lastName}`;
  }
```
***

* In general, a JavaScript variable - _a string, boolean or number, but also an object, array or function_ - is declared with a **camelCase** variable name.
***

* Avoid underscores in your names.
***

* booleans: ifThenStatements
- Example: isCarSold/carIsSold
- Make booleans that can be read well in if then statements: if carIsSold ...
- A prefix like **is**, **are** or **has** helps every JavaScript developer to distinguish a boolean from another variable by just looking at it. Example:
```
  // bad
  var visible = false;

  // good
  var isVisible = true;
```
***

* Identical to JavaScript functions, a **method** on a JavaScript class is declared with **camelCase** (use a verb as a prefix).
***

* A private variable/funcion/method has an underscore as a prefix. Example:
```
  _getName()
  _isGood()
  _myCar
```
***

* class: class NounNoun
- Use nouns for class names.
- A JavaScript class is declared with a **PascalCase** in contrast to other JavaScript data structures. Example:
```
  class SoftwareDeveloper{
    // ...
  }
```
- Also, a **component**, commonly used in frameworks, must be declared using **PascalCase**, too.
***
* Capitalize two-letters acronym. Example:
```
  let IO;
  let modifiedIO;
```
***

* Avoid large functions.
***

* Avoid code repetition.
***

* Stop writing comments - Code must speak for itself!
***

* constants:
- Write JavaScript constants with uppercase, and if there are multiple names, use underscore between them. Example:
```
  const SECONDS;
  const HOURS_PER_DAY;
```
***

* A global JavaScript variable is written in camelCase if it is mutable (normal name... with _var_ or _let_).
***

* A global JavaScript variable is written in UPPERCASE if it is immutable (using _const_ keyword).
***

* Avoid one-letter variable names.
- If you do use a single-letter variable name, limit them to small functions or as index variables in loops. Example:
```
  function getTomorrow(today) {
    const d = new Date(today);
    d.setDay(d.getDay() + 1);
    return d;
  }

  // or in for loop
  for(let i = 0; i < 100; i++) {
    // ...
  }
```
***

* Don't use a _"magic number"_. Example:
```
  // bad
  if(password.value.length < 8) {
    // ...
  }

  /*
  use:
  const = MINIMUM_PASSWORD_LENGTH = 8;
  instead of the "magic number" 8
  */

  // good
  if(password.value.lenth < MINIMUM_PASSWORD_LENGTH) {
    // ...
  }
```
***

* Always end your **switch** statements with a **default**. Even if you think there is no need for it.
***

* The **==** comparison operator always converts (to matching types) before comparison.
***

* The **===** operator forces comparison of values and types.
***

* Hyphens (this-hyphen) are not allowed in JavaScript names.
***

* Use lowercase file names.
***

* Avoid global variables. Global variables and functions can be overwritten by other scripts. All variable used in a function should be declared as local variables.
***

* In JavaScript frontend applications, you will often see PascalCase for naming components. In contrast, in JavaScript backend applications, **kebab-case** is the common sense.
***

* Use 2 spaces for indentation of code blocks. Example:
```
  function toCelsius(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);  
  }
```
- Do not use tabs (tabulators) for indentation. Different editors interpret tabs differently.
***

* Always put spaces around operators (= + - * /) and after commas. Example:
```
  var x = y + z;
  var cars = ["Audi", "BMW", "Citroen"];
```
***

* Never declare number, string or boolean objects.
- Use **" "** instead of **new String()**;
- Use **0** instead of **new Number()**;
- Use **false** instead of **new Boolean()**;
- Use **[ ]** instead of **new Array()**;
- Use **/ ( ) /** instead of **new RegExp()**;
- Use **function** instead of **new Function()**.
***

* General rules for complex (compound) statements:
[use K&R style or **TOTBS** - _The One True Brackets Style_]
- Put the opening bracket at the end of the first line;
- Use one space before the opening bracket;
- Put the closing bracket on a new line, without leading spaces.
***

* For readability, avoid lines longer than 80 characters. If a JavaScript statement does not fit on one line, the best place to break it, is after an **operator** or a **comma**.
***

* Avoid using eval().
- The eval() function is used to run text as code. In almost all cases, it should not be necessary to use it.
- Because it allows arbitrary code to be compiled, it also represents a security problem.
***
