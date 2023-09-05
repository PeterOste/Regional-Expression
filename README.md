# Regex Riddles

In this tutorial, you will learn the fundamentals of regular expressions, commonly referred to as "regex." Regex is a powerful tool for pattern matching and text manipulation. By the end of this tutorial, you'll have a solid understanding of how to create and use regex patterns effectively.

## Summary

In this tutorial, we will explore various aspects of regex by dissecting a sample JavaScript regex pattern: 

`const regexPattern = /^([A-Za-z]+)@\w+\.\w+$/;`

We will break down this regex pattern and explain each component, including anchors, quantifiers, the OR operator, character classes, flags, grouping and capturing, bracket expressions, greedy and lazy matching, boundaries, back-references, and look-ahead and look-behind assertions in the context of JavaScript.

By exploring these components with code snippets and examples, you'll gain a deep understanding of regex in the context of JavaScript. Feel free to explore each section to enhance your regex skills further.

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

In this section, we will dive deeper into the various components of the JavaScript regex pattern mentioned earlier.

### Anchors

Anchors are the markers which specify where a match should start or end within the input text.

- `^` asserts the start of the line or string.
- `$` asserts the end of the line or string.

We'll explore how to use these anchors effectively and provide examples of their usage.

**Example:**
```javascript
const regex = /^Hello/; // Matches if the string starts with "Hello"
const regex2 = /World!$/; // Matches if the string ends with "World!"

### Quantifiers

Quantifiers are used to determine how many times a specific character or group should appear in the input text. Commonly used quantifiers include:

- `*`: Matches zero or more occurrences.
- `+`: Matches one or more occurrences.
- `?`: Matches zero or one occurrence.
- `{}`: Specifies a specific range of occurrences.

**Example:**

const regex = /\d{2,4}/; // Matches 2 to 4 consecutive digits
const regex2 = /a+b*c?d/; // Matches patterns like "ad", "aabbd", "abcd"

### OR Operator

The OR operator (`|`) allows you to match one of multiple patterns. It can be used to create alternatives. For example, 
`(cat|dog)` would match either "cat" or "dog."

**Example:**

const regex = /apple|banana/; // Matches "apple" or "banana"

### Character Classes

Character classes define sets of characters that can match at a specific position in the input text. In JavaScript regex, you can create custom character classes using square brackets (`[]`). For instance, `[A-Za-z]` matches any uppercase or lowercase letter.

**Example:**

const regex = /[0-9]/; // Matches any single digit
const regex2 = /[aeiou]/; // Matches any vowel

### Flags
Flags provide additional options for regex patterns in JavaScript. Two common flags are:

- `i` (case-insensitive): Makes the pattern match regardless of letter case.
- `g` (global): Searches for all occurrences of the pattern in the input string, not just the first one.

**Example:**

const regex = /example/i; // Matches "example" case-insensitively
const regex2 = /\d+/g; // Matches all sequences of digits in the input

### Grouping and Capturing

Grouping and capturing allow you to isolate parts of a regex pattern for further use. In JavaScript regex, you can create groups using parentheses. For example, `(\d{2})-(\d{2})-(\d{4})` captures day, month, and year in a date.

**Example:** 

const regex = /(\d{2})-(\d{2})-(\d{4})/;
const match = regex.exec('05-12-2023');
console.log(match[1]); // Captures '05' (day)
console.log(match[2]); // Captures '12' (month)
console.log(match[3]); // Captures '2023' (year)

### Bracket Expressions

Bracket expressions in JavaScript regex provide a way to match a range of characters. For instance, `[A-Z]` matches any uppercase letter.

**Example:** 

const regex = /[A-F]/; // Matches uppercase letters from A to F

### Greedy and Lazy Match

Greedy and lazy matching affect how regex quantifiers behave in JavaScript. Greedy quantifiers attempt to match as much as possible, while lazy quantifiers match as little as possible.

**Example:** 

const greedyRegex = /".*"/; // Greedy match, matches the whole string within double quotes
const lazyRegex = /".*?"/; // Lazy match, matches the smallest string within double quotes

### Boundaries

In JavaScript regex, boundaries are crucial for matching whole words or specific positions within words. `\b` asserts a word boundary, while `\B` asserts a non-word boundary.

### Back-references

Back-references in JavaScript regex allow you to refer back to captured groups within the same pattern. For instance, `(\w+) \1` matches repeated words.

**Example:** 

const regex = /(\w+) \1/; // Matches repeated words like "hello hello"

### Look-ahead and Look-behind

Look-ahead (`(?=...)`) and look-behind (`(?<=...)`) assertions are advanced regex techniques in JavaScript. They allow you to assert that a particular pattern is or isn't ahead or behind the current position.

**Example:**

const regex = /foo(?=bar)/; // Matches "foo" only if it's followed by "bar"

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
