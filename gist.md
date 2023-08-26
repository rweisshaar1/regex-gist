# Gist Regex Tutorial

## Summary

In this Gist, I will discuss the Email validation Regex, and all of the different methods used in the regex. I will also explain how these methods are used to help determine if a given email address is valid or not! Here is the example email verification Regex:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

There are two symbols that are know as anchors in regex. The `^` and the `$`.

The `^` symbol is an anchor that signifies a string value that begins with the character that follows it. For example `^Hi`, would find all of the instances of "Hi" in a string of text. It would not, however, find all of the instances of "hi", for the anchor is case sensitive.

The `$` symbol is an anchor that signifies a string value that ends with the characters that come before it. Similar to the `^` anchor, the `$` anchor can be preceded by an exact matching string, or by a range of possible matches.

Looking at our email regex, you can see we have both the `^` and the `$` in use. These are both essential to our email regex.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Quantifiers

There are four different types of Quantifiers that can be used to specify your Regex: 
  - `*` The Star symbol matches a pattern anywhere from zero and up. 
  - `+` The Plus sign matches a pattern that has one or more instances.
  - `?` The Question Mark matches with a pattern that is introduced zero, or one time.
  - `{}` The curly braces give you three different ways to limit a search:
    - `{n}` limits your search by exactly "n" number of times.
    - `{n,}` limits your search by at least "n" number of times.
    - `{n,x}` limits your search by a minimum of "n" and a maximum of "x" number of times.

If we look at our regex, we can see that there are a few different quantifiers at play.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
We have the `+`, verifying that we have at least one or more of the pattern in the first section of the email, and the `{2,6}`, saying we should have a minimum of 2 characters, and a maximum of 6 at the end of the string. Both of these quantifiers help us limit our search results to what an email should have. 

### Grouping Constructs

In Regex, any subpattern enclosed within the parentheses `()` is considered a group. You can group any numbers, letters, or characters within `()` to help validate or limit your searches.  Lets take a look at our example email validation regex to see how the parentheses are being used:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
In this instance, we are using `()` in a few different spots to help group different parts of our email string. This signifies that within each of the parentheses, we would like any of those specific characters in order to validate the email.

### Character Classes

The `[]` brackets help you to define a character set, which is a set of characters you want to match in your regex. It can be specific letters or numbers, such as `[abc]`, or it can be a grouping of letters or numbers, such as `[0-9]`. In our email validation example, `[]` are used through out the regex to ensure that we have the specific characters needed within an email:
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
In the first part, we are checking if there are any letters (anything a-z) and some numbers (0-9), along with some characters.

### Character Escapes
The `\` is called the character escape, which restores the original meaning of the following character. This is essential for any validator where a character might be used more than once in a particular section, under different circumstances. It is used multiple times in our email validator, to ensure the correct usage of the regex. For example, here: `([a-z0-9_\.-]+)`

## Author

Author, Robbie Weisshaar, is currently a student at the U of M, studying to be a Web Developer. Here is a link to his GitHub:
https://github.com/rweisshaar1
