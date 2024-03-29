# A refresher on regex

## Conceptual Knowledge

### Lesson 1: Introduction to Regular Expressions

1. What are regular expressions?
        
    Regular expressions, often abbreviated as regex or regexp, are powerful text-processing patterns used to search for, match, and manipulate strings of text. They provide a concise and flexible way to describe complex text patterns.

2. Why are regular expressions useful in Python?
        
    Regular expressions are essential for text processing tasks such as data validation, text extraction, and search operations. They are widely used in Python for tasks like parsing log files, validating user input, and web scraping.

3. Basic use cases for regular expressions
        
    Regular expressions can be used to:
        - Validate email addresses and phone numbers.
        - Extract data from unstructured text.
        - Find and replace text patterns in documents.
        - Search for specific words or phrases in text.

#### Lesson 2: Character Classes and Literals


1. What are character classes and literals?
   
        Character literals are specific characters that you want to match exactly. For example, "a" will match the character "a" in a string.

        Character classes are enclosed in square brackets [] and allow you to specify a set of characters to match. For example, [aeiou] will match any vowel.

2. How to match specific characters using literals
        
        To match a specific character, simply use that character as a literal in your regex pattern. 
        
        For example, "cat" will match the string "cat" in the text.

3. Using square brackets for character classes
        
        Square brackets allow you to create a character class to match any character within them. 
        
        For example, [aeiou] will match any vowel in a string.

4. Examples and exercises for matching single characters
        
        Examples: "Hello, world!" can be matched with "H", "e", "o", ",", " ", and so on.

        Exercises: Match all lowercase letters, match all digits, match all punctuation marks.

### Lesson 3: Special Characters

1. Understanding special characters like ".", "*", "+", "?", "^", and "$"
        
        Special characters in regex have special meanings and are used to match more complex patterns.

        For example, "." matches any character except a newline, "*" matches zero or more of the preceding element, "+" matches one or more, and "?" matches zero or one.

2. How to use special characters to match **patterns**
   
        Special characters can be combined with character literals and character classes to match specific patterns.

        For example, "ca*t" will match "ct", "cat", "caat", and so on.

3. Examples and exercises for matching patterns with special characters
        
        Examples: Match any word with "w.rd" (e.g., "word," "ward," "w3rd").

        Exercises: Match URLs that start with "http://" or "https://".

Lesson 4: Quantifiers

1. Introducing quantifiers like "{n}", "{n,}", "{n,m}"

        Quantifiers allow you to specify how many times a character or group should be repeated.

        "{n}" matches exactly n occurrences, "{n,}" matches at least n occurrences, and "{n,m}" matches between n and m occurrences.

2. How to use quantifiers for repetitive patterns
        
        Quantifiers are helpful for matching repetitive patterns like dates, phone numbers, or repeated characters.

        For example, "\d{3}-\d{2}-\d{4}" matches a standard date format like "09-25-2023."

3. Examples and exercises for matching repeated patterns
        
        Examples: Match valid phone numbers with various formats, such as "(555) 555-5555" or "555-5555."

        Exercises: Match valid email addresses with different domains, such as "user@example.com" or "contact@mywebsite.co.uk."


### Lesson 5: Alternation and Groups

1. Using "|" for alternation
        
        The pipe symbol "|" is used for alternation, allowing you to match one pattern or another.

        For example, "cat|dog" will match either "cat" or "dog" in a text.

2. Creating and using capturing groups with parentheses
        
        Parentheses () are used to create capturing groups. They allow you to group parts of a pattern and apply quantifiers or alternation to the entire group.

        For example, "(ab)+" will match one or more repetitions of "ab" in a string.

3. Examples and exercises for alternation and grouping
        
        Examples: Match words that start with "apple" or "banana" using "(apple|banana)".

        Exercises: Match phone numbers in either "(555) 555-5555" or "555-5555" formats.

### Lesson 6: Character Classes and Shorthand

1. How to use predefined character classes like "\d", "\w", "\s"
        
        Predefined character classes provide shortcuts for commonly used character groups.

        "\d" matches any digit, "\w" matches any word character (letters, digits, or underscores), and "\s" matches any whitespace character.

2. Using shortcuts like "\D", "\W", "\S"
        
        The capital versions of predefined character classes negate the matching.

        "\D" matches any character that is not a digit, "\W" matches any character that is not a word character, and "\S" matches any character that is not whitespace.

3. Examples and exercises for using character classes and shortcuts
   
        Examples: Match all the digits in a string using "\d+", match all non-alphanumeric characters using "\W".
        Exercises: Match lines containing only whitespace characters, match lines that don't contain any vowels.

### Lesson 7: Anchors

 1. Understanding anchors like "^" (start of string) and "$" (end of string)
   
        Anchors allow you to specify where in the string a match should occur.

        "^" matches the start of a string, and "$" matches the end.

2. How to use anchors for precise matching
        
        Anchors are crucial for ensuring that your pattern matches exactly where you intend.

        For example, "^abc" will match "abc" only if it appears at the beginning of a string.

3. Examples and exercises involving anchors
        
        Examples: Match lines in a text that start with "Chapter" using "^Chapter".

        Exercises: Match lines in a text that end with a period ".", match lines that contain the word "Python" at the beginning of a line.

### Lesson 8: More Advanced Concepts

1. Lookaheads and lookbehinds
        
        Lookaheads (positive and negative) and lookbehinds (positive and negative) allow you to match patterns based on what precedes or follows the current position in the string.
        They are useful for more complex matching scenarios.

2. Non-capturing groups
        
        Non-capturing groups, denoted as "(?:...)", allow you to group patterns without capturing the matched text. This can be helpful for improving performance or simplifying your regular expressions.

3. Examples and exercises for advanced concepts
        
        Examples: Match email addresses that are not part of URLs, use lookaheads to match numbers followed by "USD."
        
        Exercises: Match phone numbers that are not part of email signatures, use non-capturing groups to match optional prefixes.

### Lesson 9: Practical Applications

1. Real-world examples of using regular expressions in Python
        
        Showcase practical applications such as parsing log files, extracting data from HTML, validating user input forms, and searching for specific patterns in a large dataset.

2. How to search for patterns in text
        
        Demonstrate how to use the re.search() function in Python to find the first occurrence of a pattern in a string.

3. How to extract specific information from text using regex
        
        Provide examples of using regular expressions to extract data like email addresses, URLs, dates, and phone numbers from text.

### Lesson 10: Best Practices and Resources

1. Best practices for writing efficient and readable regular expressions
        
        Discuss best practices, such as using comments, breaking complex patterns into smaller parts, and testing patterns thoroughly.

2. Recommended online resources and tools for practicing and testing regex patterns

         helpful websites, tutorials, and regex testing tools like RegExr or regex101.com.

3. Common mistakes to avoid
        
        Highlight common mistakes like excessive complexity, inefficient patterns, and not considering edge cases.

## Practical knowldege

### some python code

```python
import re

# Sample text for testing regular expressions
sample_text = """
Alice's email is alice@example.com, and Bob's email is bob@example.org.
You can reach them at (555) 123-4567 or (555) 987-6543. They live at
123 Main St., Wonderland. The date today is 09-30-2023. Please contact
them if you have any questions.
"""

# Lesson 2: Character Classes and Literals
# Matching single characters using literals and character classes
match_a = re.findall(r'a', sample_text)
match_vowels = re.findall(r'[aeiou]', sample_text)
print("Match 'a':", match_a)
print("Match vowels:", match_vowels)

# Lesson 3: Special Characters
# Matching patterns with special characters
match_emails = re.findall(r'\S+@\S+', sample_text)
match_dates = re.findall(r'\d{2}-\d{2}-\d{4}', sample_text)
print("Match emails:", match_emails)
print("Match dates:", match_dates)

# Lesson 4: Quantifiers
# Matching repeated patterns
match_phone_numbers = re.findall(r'\(\d{3}\) \d{3}-\d{4}|\d{3}-\d{4}', sample_text)
print("Match phone numbers:", match_phone_numbers)

# Lesson 5: Alternation and Groups
# Using alternation and capturing groups
match_names = re.findall(r'(Alice|Bob)', sample_text)
print("Match names:", match_names)

# Lesson 6: Character Classes and Shorthand
# Using predefined character classes and shortcuts
match_digits = re.findall(r'\d', sample_text)
match_whitespace = re.findall(r'\s', sample_text)
print("Match digits:", match_digits)
print("Match whitespace:", match_whitespace)

# Lesson 7: Anchors
# Using anchors to match patterns at the start and end
match_start_with_Alice = re.findall(r'^Alice', sample_text)
match_end_with_question = re.findall(r'\?$', sample_text)
print("Match start with 'Alice':", match_start_with_Alice)
print("Match end with '?':", match_end_with_question)

# Lesson 8: More Advanced Concepts
# Using lookaheads and non-capturing groups
match_lookahead = re.findall(r'(?=contact)Alice', sample_text)
match_non_capturing_group = re.findall(r'(?:Alice|Bob)', sample_text)
print("Match 'Alice' followed by 'contact':", match_lookahead)
print("Match names (non-capturing group):", match_non_capturing_group)

# Final Project: Regex Project
# Extracting emails and phone numbers from the sample text
extracted_emails = re.findall(r'\S+@\S+', sample_text)
extracted_phone_numbers = re.findall(r'\(\d{3}\) \d{3}-\d{4}|\d{3}-\d{4}', sample_text)
print("Extracted emails:", extracted_emails)
print("Extracted phone numbers:", extracted_phone_numbers)
```


