# Regex Gist 

The purpose of this gist is to walk through what Regex (regular expression) is. Regex is a sequence of characters that specifies a search pattern in text. This tutorial will follow the different components of a singular regular expression.

## Summary

In this tutorial, we will analyzing the Regex expression 

```javascript
 /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

which is used to match Hex values. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

The anchors in this regex example are ``` ^ ``` and ```$```

``` ^ ``` indicates the beginning of the expression that starts with a #, and ```$``` indicates the end of the expression.


### Quantifiers

The quantifiers in this regex example are ```#?``` and ```{3}``` and ```{6}```

The ```?``` is a boolean value, which must match 0 or 1 and the preceding character is ```#```, which is optional. 

```{3}``` and ```{6}``` specifies that exactly 6 or 3 of the preceding characters should be matched.


### OR Operator

The ```|``` (pipe) character is used as the OR operator in this expression. It separates two regex patterns and matches either the pattern before or after it.

### Character Classes

The character classes in this expression are determined by the square brackets, which are ```[a-f0-9]```. They are used twice in this regular expression because one has a quantifier of 3 and the other has a quantifier of 6. ```a-f``` means any letter from A to F, and ```0-9``` means any number from 0-9. They are together because they are combined. 


### Flags

A flag in a regular expression is a special character that changes the way the regular expression is interpreted and in this expression, there are none. 

### Grouping 

Grouping is anything between the ```()```, and in this regular expression, the whole thing is grouped together. 

### Bracket Expressions

A bracket expression is a special notation in square brackets that matches any one of the characters or character ranges specified inside the brackets. They can be used to specify a set of characters that you want to match in a string.

In this regex, the bracket expression is ```([a-f0-9]{6}|[a-f0-9]{3})```, which is used to match either:

```[a-f0-9]{6}``` : exactly 6 characters that are either lowercase letters between "a" and "f" or digits between "0" and "9"

```[a-f0-9]{3}``` : exactly 3 characters that are either lowercase letters between "a" and "f" or digits between "0" and "9"


### Greedy and Lazy Match

A greedy match will match the largest possible string that fits the pattern, while a lazy match will match the smallest possible string that fits the pattern.

In this expression, there is no greedy or lazy match as the quantifiers ```{6}``` and ```{3}``` are used to match exactly 6 or 3 characters, so there is no need to specify whether it should be greedy or lazy.

### Boundaries

The boundaries represent the start and end of a line. In this expression, they are the anchor points ```^``` (start) and ```$``` (end)

### Back-references

A back reference in regular expressions is a way to reuse a previously matched group in the same regular expression. It is done by using a  ```\()``` followed by the group number, and there are none in this expression. 

### Look-ahead and Look-behind

Look-ahead and look-behinds are constructs in regular expressions that allow you to check the text that comes before or after the current position without including it in the match. They are written as ```(?=...)``` and ```(?<=...)```. There are none in this regular expression.

## Author

Amanda Pietsch: https://github.com/apietsch4117
