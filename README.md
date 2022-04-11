# Regex-Gist

Introductory paragraph (replace this with your text)

## Summary

I will be explaining, in depth, the URL regex. 

* Matching a URL: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## A break down of this regex.

^(https?:\/\/)?
* At the very begining we are looking for https with the 's' being optional followed by ':' then escape char '/' '/' 
twice. Equals https:// or http:// which are both optional since the group is followed by a '?'

([\da-z\.-]+)\.
* In this group we are looking for any digit or lowercase letter or any character except a new line with a range that 
could match any. The '+' meaning it could be 1 or more. Followed by an escape character then a '.' The meat of the URL.

([a-z\.]{2,6}
* Looking for the extension here. Any lowercase letter with a min of 2 and max of 6 except a new line.

([\/\w \.-]*)*\/?$
* This would be the route or appended URL section. Assuming the url is complete this section will be optional and at 
the very end of the string. This group here we are searching for '/' any word or range that matches any with 0 or 
more. Then followed by another 0 or more and another '/' with all of this being optional.

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

* This regex uses ^ and $ to signal what needs to be at the beginning (https:// or http://), and end (/words/words). Both of these groups being optional since they are followed by the ? quantifier.

### Quantifiers

* The ? quantifier is used twice in this regex. First because the https:// or http:// really is not required for a URL to work in most cases.  Then again for an appended URL or route.

### Grouping Constructs

* This regex uses 4 main Grouping Constructs. First is matching the https:// or http:// which are both optional. Next is finding the www. or www3. Third is the meat of the URL which really could be anything. Finally an appended URL or route, which also optional.

### Bracket Expressions

* Url matching uses a few of these. First is any digits or a-z (all lowercase) for the www section \.+ then the actual domain name which could be anything.

### Character Classes

* We only use one here to find all digits that could be part of the www section.

### The OR Operator

* OR is defined using a pipe (|). We do noto use any OR's in this expression.

### Flags

* Flags are used to define things like Global or New Lines, we do not use any of these in this regex.

### Character Escapes

* A couple of Character Escapes are used in this expression since we are looking for '/' or '.', in order for use to find the 'actual' character we need to escape them since they are part of Metacharacters or Quantifiers. 

## Author

I'm just a MERN stacker trying to find my way through life. <https://github.com/iannicholas>