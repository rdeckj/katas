# String Calculator
Inspired by [Roy Osherove](https://osherove.com/tdd-kata-1/)

## Summary
Create a calculator that will take input as a string and return the sum.

## Before you begin
* Try not to read ahead
* Complete one step at a time
* Test only valid input

### Step 1 - Create a method
Create a method with the signature: `int Add(string numbers)`
* This method can take up to two positive numbers, separated by commas, and will return their sum.

For example:
* `"", "1", or "1,2"` as inputs.
* For an empty string, the method will return 0.

### Step 2 - Unknown input length

Allow the method to handle an unknown amount of numbers.

### Step 3 - Handle new lines between numbers
The following input is valid: `1\n2,3`

The following input is NOT valid: `1,\n`

### Step 4 - Support different delimiters:

To change a delimiter, the beginning of the string will contain a separate line with the format: `//{delimeter}`

For example:
* `“//;\n1;2”` should return 3, where the default delimiter is `;`

Changing a delimiter is optional. All existing scenarios should still be supported.

### Step 5 - Handle negatives
Calling `Add` with a negative number will throw an exception `negatives not allowed: {negatives}`. Where `{negatives}` contains the negative that was passed 

If there are multiple negatives, show all of them in the exception message.

For example:
* `"-1,2,-3"` should return `negatives not allowed: -1,-3`

### Step 6 - Ignore large numbers
Numbers bigger than 1000 should be ignored

For example:
* `"2,1001"` should return 2

### Step 7 - Delimiters of any length
Delimiters can be of any length with the following format: `“//[delimiter]\n”`

For example:
* `“//[***]\n1***2***3` should return 6

### Step 8 - Multiple delimiters
Allow multiple delimiters, where the first line with the format: `//[delimiter1][delimiter2]\n` 

For example:
* `“//[*][%]\n1*2%3”` should return 6
