# A refresher on regex

## Lesson 1: Introduction to Regular Expressions

1. What are regular expressions?
        
        Regular expressions, often abbreviated as regex or regexp, are powerful text-processing patterns used to search for, match, and manipulate strings of text. They provide a concise and flexible way to describe complex text patterns.

2. Why are regular expressions useful in Python?
        
        Regular expressions are essential for text processing tasks such as data validation, text extraction, and search operations. They are widely used in Python for tasks like parsing log files, validating user input, and web scraping.

3. Basic use cases for regular expressions
        
        Regular expressions can be used to:
            Validate email addresses and phone numbers.
            Extract data from unstructured text.
            Find and replace text patterns in documents.
            Search for specific words or phrases in text.

## Lesson 2: Character Classes and Literals


1. What are character classes and literals?
   
        Character literals are specific characters that you want to match exactly. For example, "a" will match the character "a" in a string.
        Character classes are enclosed in square brackets [] and allow you to specify a set of characters to match. For example, [aeiou] will match any vowel.

2. How to match specific characters using literals
        
        To match a specific character, simply use that character as a literal in your regex pattern. For example, "cat" will match the string "cat" in the text.

3. Using square brackets for character classes
        
        Square brackets allow you to create a character class to match any character within them. For example, [aeiou] will match any vowel in a string.

4. Examples and exercises for matching single characters
        
        Examples: "Hello, world!" can be matched with "H", "e", "o", ",", " ", and so on.
        Exercises: Match all lowercase letters, match all digits, match all punctuation marks.

## Lesson 3: Special Characters

1. Understanding special characters like ".", "*", "+", "?", "^", and "$"
        
        Special characters in regex have special meanings and are used to match more complex patterns.
        For example, "." matches any character except a newline, "*" matches zero or more of the preceding element, "+" matches one or more, and "?" matches zero or one.

    How to use special characters to match patterns
        Special characters can be combined with character literals and character classes to match specific patterns.
        For example, "ca*t" will match "ct", "cat", "caat", and so on.

    Examples and exercises for matching patterns with special characters
        Examples: Match any word with "w.rd" (e.g., "word," "ward," "w3rd").
        Exercises: Match URLs that start with "http://" or "https://".

Lesson 4: Quantifiers

    Introducing quantifiers like "{n}", "{n,}", "{n,m}"
        Quantifiers allow you to specify how many times a character or group should be repeated.
        "{n}" matches exactly n occurrences, "{n,}" matches at least n occurrences, and "{n,m}" matches between n and m occurrences.

    How to use quantifiers for repetitive patterns
        Quantifiers are helpful for matching repetitive patterns like dates, phone numbers, or repeated characters.
        For example, "\d{3}-\d{2}-\d{4}" matches a standard date format like "09-25-2023."

    Examples and exercises for matching repeated patterns
        Examples: Match valid phone numbers with various formats, such as "(555) 555-5555" or "555-5555."
        Exercises: Match valid email addresses with different domains, such as "user@example.com" or "contact@mywebsite.co.uk."