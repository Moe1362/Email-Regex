# Matching an Email Regex


I invite you to explore this inclusive tutorial guide on email regular expression (regex) matching, employing JavaScript in the domain of Computer Science. By the end of this tutorial, individuals new to the subject as well as scholars will gain a thorough grasp and knowledge of regex elements. This will be accomplished through in-depth explanations and analyses of practical examples. Within this tutorial, our focus will be on email regex, where we will deconstruct the constituents of a regexes pattern formulated to authenticate email addresses. We will elucidate how each component plays a role in guaranteeing precise and dependable email validation.


## Summary
In this tutorial, we will consistently refer to the provided regular expression (regex) displayed below for the purpose of analyzing each regex component. This approach aims to facilitate a comprehensive understanding for both beginners and experts, ensuring clarity in comprehending the material. The regex components covered in this guide comprise Anchors, Quantifiers, Grouping Constructs, Bracket Expressions, Character Classes, and finally Character Escapes. By thoroughly examining these elements, readers will gain a solid grasp of the topic.

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

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

Regular expressions are robust instruments for detecting patterns in text. Anchors, which are special characters in regular expressions, are pivotal in determining the position of a pattern within a given input string. When it comes to email validation, as exemplified by the regex showcased in this tutorial /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, it is of utmost importance to verify that the entire input string precisely matches the specified pattern, rather than merely a portion of it.

### Quantifiers

In typical expressions (regex), quantifiers serve the purpose of indicating the desired number of matches for a pattern. These quantifiers are positioned after a character, character class, or group, enabling the specification of the minimum and maximum occurrence range for the preceding pattern.

The + quantifier signifies "one or more" and is applied after the pattern [a-z0-9_\.-] within the first capturing group ([a-z0-9_\.-]+). This implies that the pattern [a-z0-9_\.-] must appear at least once, but it can also appear consecutively multiple times. As a result, the group will match a sequence of one or more lowercase letters, digits, underscores, dots, or hyphens.

Likewise, the + quantifier is employed after the pattern [\da-z\.-] within the second capturing group ([\da-z\.-]+). This particular group corresponds to one or more occurrences of digits, lowercase letters, dots, or hyphens.

The {2,6} quantifier is applied after the character class [a-z\.] within the third capturing group ([a-z\.]{2,6}). This specific group corresponds to a sequence of 2 to 6 lowercase letters or dots. Consequently, this indicates that the email address should conclude with a top-level domain comprising two to six letters, such as .com, .edu, or .co.uk.

Combining all the components, the following regular expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ can be used to identify a valid email address. The email address should begin with one or more lowercase letters, digits, underscores, dots, or hyphens, followed by the @ symbol. After that, it should have one or more digits, lowercase letters, dots, or hyphens. Finally, it should end with a period and a top-level domain consisting of two to six letters.

Given the regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`:

1. Quantifier `+` : Matches "one or more" occurrences.
   - `([a-z0-9_\.-]+)`: Matches one or more lowercase letters, digits, underscores, dots, or hyphens.
   - `([\da-z\.-]+)`: Matches one or more digits, lowercase letters, dots, or hyphens.

2. Quantifier `{2,6}` : Matches between 2 and 6 occurrences.
   - `([a-z\.]{2,6})`: Matches a sequence of 2 to 6 lowercase letters or dots.


The regex above matches valid email addresses with the following pattern:
- One or more lowercase letters, digits, underscores, dots, or hyphens
- Followed by the `@` symbol
- Followed by one or more digits, lowercase letters, dots, or hyphens
- Followed by a period
- Ending with a two to six letter top-level domain (e.g., .com, .edu, .co.uk)

### OR Operator

The OR operator allows for alternative matches, but it's not used in our email validation regex pattern.

### Character Classes

The provided email regex utilizes the core character class: \d and the character set notation: [a-z], [0-9], and [.-]. Character sets are enclosed within square brackets and allow for matching a single character from the defined range. They are a fundamental aspect of regex, enabling the representation of multiple characters within a set range.

### Flags

Flags modify the behavior of the regex engine, but none are used in our email validation regex pattern.

### Grouping and Capturing

Groups capture parts of the match for later use, but they are not explicitly used in our email validation regex pattern.

### Bracket Expressions

Bracket expressions match a single character from a specified range or set. We utilize bracket expressions to match specific characters in the email address.

### Greedy and Lazy Match

Our regex pattern uses greedy matching, ensuring that it matches as much of the string as possible while still allowing the entire regex to match.

### Boundaries

The word boundary \b ensures that the email address is matched within the boundaries of words, preventing partial matches.

### Back-references

Back-references allow referencing previously matched groups within the regex, but they are not used in our email validation regex pattern.

### Look-ahead and Look-behind

Look-ahead and look-behind assertions assert conditions before or after the current position in the text, but they are not used in our email validation regex pattern.

## Author

### Mohammad Abbasi

* [Linkedin](https://www.linkedin.com/in/mxabbasi/)
* [Github-Profile](https://github.com/Moe1362)