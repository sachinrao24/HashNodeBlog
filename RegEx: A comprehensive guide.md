---
title: "RegEx: A comprehensive guide"
seoTitle: "RegEx: A comprehensive guide"
seoDescription: "The only article you need to learn RegEx in depth and gain a deep understanding of how it works."
datePublished: Sun Mar 19 2023 12:48:31 GMT+0000 (Coordinated Universal Time)
cuid: clffe928h00010al17nr19jnm
slug: regex-a-comprehensive-guide
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679230252343/119c7ea8-15fc-492c-afdb-3cebfd4da24e.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679230039186/1e3391f7-5f42-4e8e-a461-13ca476dcbd3.png
tags: search, fundamentals, regex, programming-ciovqvfcb008mb253jrczo9ye, natural-language-processing

---

You may or may not have heard of RegEx before. Either way, this article is going to give you a solid foundation of what it is and how you can use it.

A Regular Expression, aka RegEx, can be defined as a sequence of characters used to describe a search pattern. We can then check if a given text contains the required pattern.

Let's take a look at the different components of RegEx and how they work.

### Metacharacters

These are characters that have special meanings associated with them during processing.

* **Letters**\- Letters in the alphabet such as 'a', 'b', etc. can be used to search a string.
    
    For example, by searching for "z", we can get the following example strings as results- "a**z**da", "**z**ealous" or "pi**zz**a".
    
    Multiple letters can also be used for this purpose.
    
    Eg- By searching for "ab", we may get- "F**ab**ulous" or "**ab**ility".
    
* **Caret (^)**\- This symbol is used when we want to search for a pattern present at the beginning of a text.
    
    Eg- Searching for "^s", we get strings that start with the letter 's', such as- "**s**imple" or "**s**alt".
    
* **Dollar ($)**\- This symbol is used when we want to search for a pattern present at the end of a text.
    
    Eg- Searching for "r$", we get strings that end with the letter 'r', such as- "pilla**r**" or "humo**r**".
    
* **Dot (.)**\- Used to match any single character (except the newline character, "\\n").
    
    Eg- Searching for "a.t", we get strings that have a single character between 'a' and 't', such as- "**ant**" or "**art**".
    
* **Pipe (|)**\- This is used to match patterns on either side of the symbol. If you are familiar with logical operators, you may know this as the OR operator.
    
    Eg- Searching for "a|z" matches strings that contain either 'a' or 'z'.
    
    When the character on the left is matched, the one on the right is ignored.
    
* **Backslash (\\)-** The backslash is used to remove any special meaning that other RegEx characters may have.
    
    Eg- We looked at how the dot matches any single character. But what if you wanted to search for an actual '.' in the text?
    
    You can do this by searching for- "\\."
    
    The backslash removes the special meaning of the dot symbol and gives strings such as- "www\*\*.**website**.\*\*com"
    

### Quantifiers

These are symbols used to specify the number of occurrences of a pattern.

* **Asterisk (\*)**\- Used to match 0 or more occurrences.
    
    Eg- "r\*" can match strings such as- "apple" (0 occurrences), "art" (1 occurrence) or "barren" (2 occurrences).
    
* **Plus (+)**\- Used to match 1 or more occurrences.
    
    Eg- "r+" matches only "art" (1 occurrence) or "barren" (2 occurrences).
    
* Question mark (?)- Matches only 0 or 1 occurrence.
    
    Eg- "r?" matches only "apple" (0 occurrences), "art" (1 occurrence).
    
* **{x}**\- Matches only x occurrences.
    
    Eg- "r{2}" matches only "barren" (2 occurrences).
    
* **{x,y}**\- Matches occurrences between x and y.
    
    Eg- "r{2,4}" matches strings containing 'r' twice, thrice or 4 times.
    
* **Greedy** and **lazy** matching- Greedy matching refers to matching the longest possible string represented by a pattern whereas lazy matching refers to matching the shortest possible string.
    
    Eg- Let's say we want to match HTML tags in the given string-
    
    "&lt;h1&gt;This is a sentence&lt;/h1&gt;"
    
    By specifying the regular expression- "&lt;.+&gt;", which is supposed to match the left chevron (&lt;), one or more single characters (.+) and the right chevron (&gt;), we would assume that this would match "&lt;h1&gt;" and
    
    "&lt;/h1&gt;".
    
    However, the default method of matching is greedy, i.e., it will match the longest sequence of characters, which in this case, lie between the left chevron of the &lt;h1&gt; and the right chevron of the &lt;/h1&gt; tags, which basically matches the whole string-
    
    "&lt;h1&gt;This is a sentence&lt;/h1&gt;"
    
    If we want to stop at the '&gt;', all we do is insert a question mark before the '&gt;' in our RegEx, i.e., our expression becomes- "&lt;.+?&gt;"
    
    This matches the fewest characters between two chevron arrows. This form of matching is an example of lazy matching.
    

### Groups

A collection of characters enclosed in different types of brackets represent groups.

* **Parentheses** **( )**\- Matches multiple groups of characters enclosed in the parentheses.
    
    Eg- "(.+)-(.+)" will match two groups. One group of one or more characters before the hyphen, and the other group after the hyphen. But it won't match the hyphen itself.
    
* **Curly brackets { }**\- Matches a specific number of occurrences mentioned inside the brackets. This is the same as the quantifier {x,y} which we looked at previously.
    
* **Square brackets \[ \]**\- Specifies a range of characters, out of which any single character is matched.
    
    Eg- "\[a-z\]" matches any lowercase character between a and z, while \[abc\] matches either a, b or c.
    
    Multiple ranges of characters can be specified within these brackets as well.
    
    Eg- "\[a-zA-Z0-9\]" matches lower-case and upper-case characters and digits between 0 and 9.
    
* **Non-capturing groups (?: X)**\- Non-capturing groups represent those groups that you don't want return as an output.
    
    Eg- From a string such as, "I won $10.48 today!", you may only want to capture the value of dollars and cents as two groups.
    
    For this, we can use the expression-
    
    "(?:$)(\[0-9\]+)\\.(\[0-9\]{2})"
    
    Don't let the length of the expression frighten you if you're a beginner. Let's break the expression down to understand it.
    
    "(\[0-9\]+)" represents the first group returned which contains one or more digits present between 0 and 9.
    
    "\\." represents a single dot, and eliminates the special meaning that the dot character has.
    
    "(\[0-9\]{2})" represents the second group of digits between 0 and 9. By specifying {2}, we get only two digits from this group.
    
    You might be wondering why "(?:$)" is not the first group returned. This is what we call a non-capturing group. This group is identified by the pattern, but since in this case we only want the value of dollars and not the dollar symbol itself, it is not returned as an output.
    
* **Caret symbol within square brackets** **\[^X\]**\- When we use a caret symbol within a pair of square brackets, it acts as a negation operator, i.e., it will return strings that do **NOT** contain the characters mentioned in the brackets.
    
    Eg- "\[^0-9\]" returns strings that don't have the digits 0 to 9.
    

### Shorthand character classes

* \\d- Matches one decimal digit.
    
* \\D- Matches one non-decimal digit.
    
* \\w- Matches any word character or alphanumeric character (0-9, a-z, A-Z).
    
* \\W- Matches any non-word or non-alphanumeric character.
    
* \\s- Matches one whitespace character.
    
    A few subsets of this are-
    
    * \\t- Represents one tab space character.
        
    * \\r- Represents one carriage return, i.e., the beginning of a line.
        
        ```python
        print("apple\rok")
        >>okple
        ```
        
        Eg- print("apple\\rok") will rewrite "apple" as "okple" by going to the beginning of the string and overwriting it with the characters that are specified after "\\r".
        
    * \\n- Represents a newline character.
        
        ```python
        print("apple\nok")
        >>apple
          ok
        ```
        
        Eg- print("apple\\nok") will move to a new line after printing "apple" and then print "ok".
        
    * \\f- Represents a formfeed character. Although it isn't widely used anymore, it is mainly used for giving indentations.
        
        ```python
        print("apple\fok")
        >>apple
               ok
        ```
        
* \\S- Matches one non-whitespace character.
    
* \\0- Matches a null character.
    
* \\b- Matches a word boundary, i.e., the start or end of a word.
    
    While '^' and '$' can be used to match the start and end of the entire string, we can't use them to match the start or end of individual words inside a string.
    
    Eg- Let's say we want to identify words that start with 'y' and end with 'u' in the string-
    
    "I did warn you not to trust me"
    
    (Any Game of Thrones fans?)
    
    We can use the RegEx- "\\by.+u\\b"
    
    "\\by" identifies words that start with 'y', and "u\\b" identifies words that end with 'u'.
    

### That's it!

You've reached the end! You're now ready to use RegEx as a powerful tool in your programming journey. If you want to practice and learn more about RegEx, I recommend the following websites (not sponsored)-

* [https://regex101.com/](https://regex101.com/)
    
* [https://regexr.com/](https://regexr.com/)
    
* [https://www.regular-expressions.info/](https://www.regular-expressions.info/)
    

If you found this helpful, consider liking and sharing it, and subscribing to my newsletter. Feel free to leave your thoughts, questions and ponderings in the comments.

You can also follow me for more data and ML-related content. I focus on demystifying technical jargon and encouraging newcomers in the field by explaining concepts as simply as possible.

This is Sachin being succinct :)
