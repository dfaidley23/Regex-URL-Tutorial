# Title URL Matching

I will begin explaining how the Regex for matching a URL functions in this tutorial.

## Summary

So to begin explaining how the Regex for matching a URL functions I will show you what it looks like below and then begin explaining all of the parts that make up this Regex and how they all work.

~~~
    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
~~~

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The main anchors for most of Regex compnoents are
- ^ for the beginning of the line
this represents where the string starts as an example
~~~
^Apple
~~~
The A in Apple will be the start of the string as it is preluded with the Caret (^) Anchor.

- $ will be the ending anchor for the String


### Quantifiers

Quantifiers are used to determine how many times part of your expression can or can't be repeated or even included.

For example:
~~~
function validURL(string) {
   let pattern = new RegExp('^(https?:\/\/)?')
~~~

This will validate the URL to either include or not inculde the S within HTTPS requests or simply allow it to be an HTTP request.

The reason this works is because the ? Quantifier is the option quantifier and it works simliar to hwo the ? works when you are making a URL within an app and you have option parameters for that URL.

Another common Quantifiers is the *.
This Quantifier will allow multiple characters to be used repeatedly such as
~~~
*/\
~~~
which will allow these slashes to be used multiple times in the URL string like below and it would be a valid URL.
- https://testURL/URL/Test

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

David Faidley

https://github.com/dfaidley23