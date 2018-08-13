# CleanCodeSynthesis
Short synthesis of Clean Code book by Robert C. Martin

## I. Names
* Case :
  - `UpperCamelCase` for classname
  - `UPPERCASE` for constants
  - `lowerCamelCase` for everything else
* Meaningful names, no `var1` or `a2` shit
* No need to prefix attributes with m_, it's old stuff

## II. Functions
* Function body should be small
* Functions should do one thing ONLY
* Extract blocks of code as functions whenever possible
* Use meaningful names (again)
* Use as few arguments as possible
* NEVER use arguments as output. Use return statement instead if possible. If not, that means this function should be a method of the object you want as output

## III. Comments
* Avoid writing comments, code should be self explanatory (we don't like redundancy, so don't explain yourself twice)
* If you feel the need to write a comment to explain a block of code, extract a function instead and put a meaningful name on it (again, self explanatory)
* Delete commented-out code (it's not lost code if you use a vcs)

## IV. Formatting
* Place opening brackets at the end of the line, not at the beginning of the next line
* Don't try to condense short functions or statements into a single line
* Don't be afraid of putting a space character where it's optional (like around operators, between closing parenthesis and opening brackets)
* Order the functions in your file the smart way. Imagine you had to read all the code, starting from the main function and every time you see a function call, you have to read that function (if you don't have already). Imagine you had to minimize the amount of scroll you have to accomplish to read all the code. The easy way would be to order them like you would do a pre-order tree traversal : you would put the main function first, the first function called would be second, and the first function called by this one would be third, and so on. That way, you would minimize the vertical distance between the caller (above) and the callee function (below)

#### Example
```java
public double calculateDeltaV(double gazEjectionSpeed, double shipMassInital, double shipMassFinal) {
  return gazEjectionSpeed * Math.log(shipMassInital / shipMassFinal);
}
```
