## DESCRIPTION
From those other gist that are created under Regex tutorial, they explain how regex components works.
Short for regular expression, a regex is a string of text that lets you create patterns that help match, locate, and manage text.

-----

## Table of Contents

* [DESCRIPTION](#description)
* [ANCHOR](#anchor)
* [QUANTIFIERS](#quantifiers)
* [CHARACTER CLASS](#characterclass)
* [GROUPING AND CAPTURING](#groupingandcapturing)
* [BRACKET EXPRESSION](#bracketexpression)
* [GREEDY AND LAZY MATCH](#greedyandlazymatch)
* [AUTHOR](#author)

-----

Here is an example of how regex works after researching the regex (Matching an URL):

/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

-----

## ANCHOR
For example we have "abc" for the input:

^a matches abc 
but ^b does not match with abc,
similar with ^c does not match with abc

Back to the url,
^ is following by the start of the code.
Matches the beginning of the input.

-----

## QUANTIFIERS
Quantifiers indicates number of times a set of character or expressions to match.

For example,
/to*/ matches "too" in "I like food too" and "t" in "thank you", but nothing in "sausage sauce"

These are some types of quantifiers characters:
```
* + ?
```
Back to the url,
The '?' after https means optional. Either http or https can still work. 
The '?' after (https?:\/\/) also act the same way.
{2,6} means the regex will include 2-6 characters inside [a-z\.]

-----

## CHARACTER CLASS
Character Classes distinguish in between letters and digits.

Example:
[q-z] matches "z" in "zoo"

These are some character types
```
\D \* [a-z]
```

Back to the url,
The '\w' here ([\/\w \.-]*)*\/?$/ is looking for any alphanumerical character after the . dot
another one is [a-z\.] looking for a-z letters

-----

## GROUPING AND CAPTURING
This is done by defining groups of characters and capturing them using the special parentheses ( and ) metacharacters. Any subpattern inside a pair of parentheses will be captured as a group.
This is useful for later processing when input data may be presented in a different order than desired.

Back to the url,
/^(https?:\/\/)?       http/https portion
([\da-z\.-]+)\.        application or website name
([a-z\.]{2,6})         following by a .com or .net
([\/\w \.-]*)*\/?$/    rotues for the website

-----

## BRACKET EXPRESSION
It has square brackets around it []. It is looking for similar regex inside the [].

Back to the url,
[\da-z\.-]      looking for any letters, dashes, and dots
[a-z\.]
[\/\w \.-]

-----

## GREEDY AND LAZY MATCH
Greedy: tries to repeat the quantified character as many times as possible.
Lazy: Enabled by the question mark ? after the quantifier. Tries to match the rest of the pattern before each repetition of the quantified character.

Back to the url,
{2,6} gives the greedyness of at least 2 but 6 the most characters regex.
Lazy would be the ?

-----

## AUTHOR
Shek Chun Lee, Github link https://github.com/leeshekchun
