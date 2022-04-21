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

Bracket Expressions help to identify the characters that are allowed within the expression. A lot of different expressions are possible but below I will show the \w.

In code adding \w into a String like this
~~~
[/\w/]
~~~
Means that any character or digit in the latin alphabet will be matched if they are present.

So the d in dinosaur will be matched for example.

Also for certain characters like the % sign you can use the \W for any character that is not in the Latin Alphabet.

### Character Classes

Character classes are a set of characters enclosed in square brackets. In my previous example the \w would be a character class

### The OR Operator


### Flags

Flags are a single lowersace alphabetic character used to help searching behavior.
An example of a flag would be the g glag and this would make the expression search for all occurances of any criteria that you have setup to flag like like if you wish to flag /a you would give it the flag /a/g for the Global flag

### Character Escapes
A character escape is a way to specify the search even more thouroughly like finding a single \ in the string. It will always be prepended with a backslash so this will look like /\\/


### Sources

- https://www.rexegg.com/regex-quantifiers.html
- https://www.rexegg.com/regex-anchors.html
- https://www.codeguage.com/courses/regexp/flags
- 
## Author

David Faidley

https://github.com/dfaidley23