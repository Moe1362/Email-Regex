### Matching an Email Regex

I created a tutorial and publised it in a Github gist. Through this tutorial we will consistently refer to the provided regular expression (regex) for the purpose of analyzing each regex component. This approach aims to facilitate a comprehensive understanding for both beginners and experts, ensuring clarity in comprehending the material. The regex components covered in this guide comprise Anchors, Quantifiers, Grouping Constructs, Bracket Expressions, Character Classes, and finally Character Escapes. By thoroughly examining these elements, readers will gain a solid grasp of the topic.
#
* [Github Gist Link](https://gist.github.com/Moe1362/de5586ad034c9c884ede2fa6a77183d1.js)


# Table of Contents

- Anchors
- Quantifiers
- OR Operator
- Character Classes
- Flags
- Grouping and Capturing
- Bracket Expressions
- Greedy and Lazy Match
- Boundaries
- Back-references
- Look-ahead and Look-behind

## Regex Components

# Anchors

Regular expressions are robust instruments for detecting patterns in text. Anchors, which are special characters in regular expressions, are pivotal in determining the position of a pattern within a given input string. When it comes to email validation, as exemplified by the regex showcased in this tutorial /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, it is of utmost importance to verify that the entire input string precisely matches the specified pattern, rather than merely a portion of it.

# Quantifiers

In typical expressions (regex), quantifiers serve the purpose of indicating the desired number of matches for a pattern. These quantifiers are positioned after a character, character class, or group, enabling the specification of the minimum and maximum occurrence range for the preceding pattern.

The + quantifier signifies "one or more" and is applied after the pattern [a-z0-9_\.-] within the first capturing group ([a-z0-9_\.-]+). This implies that the pattern [a-z0-9_\.-] must appear at least once, but it can also appear consecutively multiple times. As a result, the group will match a sequence of one or more lowercase letters, digits, underscores, dots, or hyphens.

Likewise, the + quantifier is employed after the pattern [\da-z\.-] within the second capturing group ([\da-z\.-]+). This particular group corresponds to one or more occurrences of digits, lowercase letters, dots, or hyphens.

The {2,6} quantifier is applied after the character class [a-z\.] within the third capturing group ([a-z\.]{2,6}). This specific group corresponds to a sequence of 2 to 6 lowercase letters or dots. Consequently, this indicates that the email address should conclude with a top-level domain comprising two to six letters, such as .com, .edu, or .co.uk.

# OR Operator

The OR operator allows for alternative matches, but it's not used in our email validation regex pattern.

# Character Classes

The provided email regex utilizes the core character class: \d and the character set notation: [a-z], [0-9], and [\.-]. Character sets are enclosed within square brackets and allow for matching a single character from the defined range. They are a fundamental aspect of regex, enabling the representation of multiple characters within a set range.

# Flags

Flags modify the behavior of the regex engine, but none are used in our email validation regex pattern.

# Grouping and Capturing

Groups capture parts of the match for later use, but they are not explicitly used in our email validation regex pattern.

# Bracket Expressions

Bracket expressions match a single character from a specified range or set. We utilize bracket expressions to match specific characters in the email address.

# Greedy and Lazy Match

Our regex pattern uses greedy matching, ensuring that it matches as much of the string as possible while still allowing the entire regex to match.

# Boundaries

The word boundary \b ensures that the email address is matched within the boundaries of words, preventing partial matches.

# Back-references

Back-references allow referencing previously matched groups within the regex, but they are not used in our email validation regex pattern.

# Look-ahead and Look-behind
Look-ahead and look-behind assertions assert conditions before or after the current position in the text, but they are not used in our email validation regex pattern.

# License

MIT License

# Author

### Mohammad Abbasi

* [Linkedin](https://www.linkedin.com/in/mxabbasi/)

* [Github-Profile](https://github.com/Moe1362)
