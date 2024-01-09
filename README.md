# Computer Science for Javascript: Regex Tutorial

This readme will introduce regex as a pattern searching tool for the users. Regex excels at returning values that the users want and it can also be used to modify the returned value. Having basic knowledge of regex is useful in technical interviews, as a lot of companies nowadays will test the interviewees on that subject.

## Summary

<!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->
Regex is a tool that is useful for searching patterns in a sea of codes. Albeit there are other ways to do the same thing, regex provides a lot of convenience, providing the users know how to use it. Regex was derived from regular expressions, and it comes from mathematics and computer science theory, where it reflects a trait of mathematical expressions called regularity [Source: O'Reilly](https://www.oreilly.com/library/view/regular-expressions-cookbook/9780596802837/ch01.html#:~:text=The%20term%20regular%20expression%20comes,that%20doesn't%20use%20backtracking.). There are also sometimes referred to as *literal* or *constructor*.

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

Anchors are a tool (or assertion) in regex family that looks for patterns at the beginning or the end of the string or line. It is very efficient because it doesn't search for the patterns anywhere else besides the end of the line or beginning of the string, therefore giving the users faster results than if you use only the normal regex.

### Quantifiers

Quantifiers filters out how many times part of your regex (character, group, or character class) was repeated, and only show the results that met the criteria you specified (aka how many times you want it to be in order for the search to go through).

A couple of the quantifiers are: 

* **\b** : Start or end at a word boundary

* **an+** : Matches an a followed by one or more n characters

* __\w*?__ : Matches a word character zero or more times but as few times as possible

[Source: www.markdownguide.org](https://www.markdownguide.org/basic-syntax/#:~:text=To%20bold%20text%2C%20add%20two,without%20spaces%20around%20the%20letters.&text=I%20just%20love%20**bold,bold%20text.)

### Grouping Constructs

Grouping is a very powerful tool of regex that allows you to search a series of characters as a group. It will search any patterns that matches what you typed in, even if it's part of a string (unless you specified otherwise). It is very useful when you need to find or verify only phone number (of certain formats) or emails in a series of text.

### Bracket Expressions

Bracket expression will match any characters inside it. It can be used as "[a-d]" to indicate any characters ranging from a to z in lower case. "(/[a-d]/i)" will make it so it's not case sensitive. "{}" will match a string according to the number you put in the curly bracket. For example, "(/ha{3}/)" will only matches "bahahaha" but not "haha".

### Character Classes

Character classes can distinguish the difference between letters, digits, and etc. "." will match any single character regardless of it's class. "\d" will match digits from "0-9". "\w" will match any alphanumeric characters from "A-Z", "a-z", and "0-9". More of character class can be found in this link [Character classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Character_classes)

### The OR Operator

QR operator is used to store a regex as a reference in a variable. It is useful when you need to use the same regex more than a few times, as you don't have to retype the same pattern again.

### Flags

Flags are modifier that alters the default searching behavior of a regex. It is usually placed right behind the second lash in any regex: "/regex/*flags*".

Below are a couple examples of flags:

* **i** : Ignore case sensitivity

* **g** : Search globally

* **s** : Make "." match newlines

* **m** : Makes "^" and "$" match the start and end of every line instead of every string

* **y** : Stands for *sticky*. Sticky uses the lastIndex property. The "y" flag indicates that the regex attempts to match the target string only from the index indicated by the *lastIndex* property. [Sticky](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp/sticky)

* **u** : Makes the expression treat characters in a given test string as code points rather than code units. This means that with the u flag set, we can get our expressions to behave normally on characters that are outside the BMP range of the UTF-16 encoding. [Unicode](https://www.codeguage.com/courses/regexp/flags)

### Character Escapes

Character Escapes are \f, \n(new line), \r, \t (tab), \v, and etc. Putting a "\" in front of the usual character will change its function, making it being represented in its literal form.

## Author

About Me: 
Github Link: [KaarageOnigiri](https://github.com/KaarageOnigiri)