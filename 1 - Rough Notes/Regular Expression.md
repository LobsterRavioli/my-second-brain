2024-09-19 11:59
Status:
Tags:
___
# Regular Expression

Regular Expression are expression of character sequences that represent patterns in text.
This pattern matching is useful for find, edit what you need.
Here are some examples of real use cases:
- Write parsing rules to HTTP servers like nginx.
- Write scripts that convert text-based dataset
- Search for occurences in journal entries or documents.
- Filter markup documents.
## Atom

An atom in regular expression it's the basic or simpliest thing that composes  a regular expression it could be a letter or these three symbols:
- `.`: It represents any character expect new line.
- `^`: It represents the beginning of the line.
- `$`: It represents the ending of the line.

##  Bracket expressions

Bracket is an atom that could be represent multiple characters.
This regular expressions  `[abc]a`   means that 'aa', 'ba' and 'ca' words will be matched.
Bracket expressions accepts class too.
There are some expressions:
Here’s the text with the character classes formatted using code:

- **`[:alnum:]`**: Represents an alphanumeric character.
- **`[:alpha:]`**: Represents an alphabetic character.
- **`[:ascii:]`**: Represents a character from the ASCII character set.
- **`[:blank:]`**: Represents a blank character, that is, a space or a tab.
- **`[:cntrl:]`**: Represents a control character.
- **`[:digit:]`**: Represents a digit (0 through 9).
- **`[:graph:]`**: Represents any printable character except space.
- **`[:lower:]`**: Represents a lowercase character.
- **`[:print:]`**: Represents any printable character including space.
- **`[:punct:]`**: Represents any printable character that is not a space or an alphanumeric character.
- **`[:space:]`**: Represents white-space characters: space, form-feed (`\f`), newline (`\n`), carriage return (`\r`), horizontal tab (`\t`), and vertical tab (`\v`).
- **`[:upper:]`**: Represents an uppercase letter.
- **`[:xdigit:]`**: Represents hexadecimal digits (0 through F).

## Quantifiers

Quantifiers in regular expressions (regex) are symbols that define how many times a character, character class, or group must occur in the input string for a match to happen. They are fundamental for making searches more flexible and powerful, particularly in Linux tools like `grep`, `sed`, and `awk`.

### **Common Quantifiers**

1. **`*` (Zero or more)**
   - Matches **zero or more** occurrences of the preceding character or group.
   - Example:
     - Regex: `ab*c`
     - Matches: `"ac"`, `"abc"`, `"abbc"`, `"abbbc"`, etc.

2. **`+` (One or more)**
   - Matches **one or more** occurrences of the preceding character or group.
   - Example:
     - Regex: `ab+c`
     - Matches: `"abc"`, `"abbc"`, `"abbbc"`, etc. 
     - Does not match: `"ac"`

3. **`?` (Zero or one)**
   - Matches **zero or one** occurrence of the preceding character or group.
   - Example:
     - Regex: `ab?c`
     - Matches: `"ac"`, `"abc"`
     - Does not match: `"abbc"`

4. **`{n}` (Exactly n times)**
   - Matches exactly **n** occurrences of the preceding character or group.
   - Example:
     - Regex: `a{3}`
     - Matches: `"aaa"`
     - Does not match: `"aa"` or `"aaaa"`

5. **`{n,}` (n or more times)**
   - Matches **n or more** occurrences of the preceding character or group.
   - Example:
     - Regex: `a{2,}`
     - Matches: `"aa"`, `"aaa"`, `"aaaa"`, etc.
     - Does not match: `"a"`

6. **`{n,m}` (Between n and m times)**
   - Matches **between n and m** occurrences of the preceding character or group.
   - Example:
     - Regex: `a{2,4}`
     - Matches: `"aa"`, `"aaa"`, `"aaaa"`
     - Does not match: `"a"` or `"aaaaa"`

---

### **Examples in Linux**

#### 1. Using `grep` with Quantifiers

- **Match lines where `a` appears zero or more times before `b`**:
  ```bash
  echo -e "b\nab\naab\nabb" | grep "a*b"
  ```
  Output:
  ```
  b
  ab
  aab
  abb
  ```

- **Match lines where `a` appears one or more times before `b`**:
  ```bash
  echo -e "b\nab\naab\nabb" | grep "a+b"
  ```
  Output:
  ```
  ab
  aab
  abb
  ```

- **Match lines with exactly 3 `a`'s**:
  ```bash
  echo -e "a\naa\naaa\naaaa" | grep "a{3}"
  ```
  Output:
  ```
  aaa
  aaaa
  ```

#### 2. Using `sed` with Quantifiers

- **Replace occurrences of two or more `a`'s with `X`**:
  ```bash
  echo "aa ab aaa aaaa" | sed 's/a{2,}/X/g'
  ```
  Output:
  ```
  X ab X X
  ```

#### 3. Using `egrep` (Extended grep)

- **Match lines where `a` occurs between 2 and 4 times**:
  ```bash
  echo -e "a\naa\naaa\naaaa\naaaaa" | egrep "a{2,4}"
  ```
  Output:
  ```
  aa
  aaa
  aaaa
  ```

---

### **Summary of Quantifiers**

Atom quantifiers are used for represent atom multiple sequences that can occur in match of the word.

| **Quantifier** | **Meaning**           | **Example** | **Matches**                          |
| -------------- | --------------------- | ----------- | ------------------------------------ |
| `*`            | Zero or more          | `ab*c`      | `"ac"`, `"abc"`, `"abbc"`, `"abbbc"` |
| `+`            | One or more           | `ab+c`      | `"abc"`, `"abbc"`, `"abbbc"`         |
| `?`            | Zero or one           | `ab?c`      | `"ac"`, `"abc"`                      |
| *`{n}`         | Exactly n times       | `a{3}`      | `"aaa"`                              |
| `{n,}`         | n or more times       | `a{2,}`     | `"aa"`, `"aaa"`, `"aaaa"`            |
| `{n,m}`        | Between n and m times | `a{2,4}`    | `"aa"`, `"aaa"`, `"aaaa"`            |

---

Using quantifiers effectively allows you to match patterns with varying lengths and repetitions, making your regex searches much more versatile.

___
## References
[[LPIC-1 Exam 101.pdf#page=]]