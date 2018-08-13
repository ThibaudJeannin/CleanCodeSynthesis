# CleanCodeSynthesis
Short synthesis of Clean Code book by Robert C. Martin

## I. Names
* Case :
  - `UpperCamelCase` for classname
  - `UPPERCASE` for constants
  - `lowerCamelCase` for everything else
* Meaningful names, no `var1` or `a2` shit
* No need prefix attributes with m_

## II. Functions
* Function body should be small
* Do one thing ONLY
* Extract blocks of code as functions whenever possible
* Use meaningful names (again)
* Use as few arguments as possible
* NEVER use arguments as output. Use return statement instead if possible. If not, that means this function should be a method of the object you want as output

## III. Comments
* Avoid writing comments, code should be self explanatory (we don't like redundancy, so don't explain yourself twice)
* Delete commented-out code (it's not lost code if you use a vcs)


## IV. Formatting
* Place opening brackets at the end of the line, not at the beginning of the next line
* Don't try to condense short functions into a single line
* Don't be afraid of putting a space character where it's optional (like around operators, between closing parenthesis and opening brackets)

#### Example
```java
public double calculateDeltaV(double gazEjectionSpeed, double shipMassInital, double shipMassFinal) {
  return gazEjectionSpeed * Math.log(shipMassInital / shipMassFinal);
}
```
