---
tags:
---

2024-09-16 15:45
Status:
Tags:
___
# Wildcards

[[Wildcards]] are very useful they can represent multiple characters.
Wildcards are used in commands like [[cp]], [[ls]], [[rm]]

Here there's some example:

- Remove everything from the current working directory
```bash
rm *
```

- Remove all files that follow this pattern where ? can be any character
```bash
rm l?st
```

- Remove all directories that starts with a letter
```bash
rmdir [a-z]*
```

# Types of Wildcards

There are 3 characters that can be used as wildcards in Linux:

- asterix `*` : zero or one or more occurences of every character
- question mark `?`: which represents a single occurence of any character.
- brackets `[` `]` which represents any occurance of the character enclosed in the square brackets

## Asterix

Find every .png file in folder home.
```bash
find /home -name *.png
```

- List every text file tha start with lpic
```bash
ls lpic-*.txt
```

- Copy all the files in the folder animal in fores
```bash
cp -r animal/* forest
```

- Remove every file that contains ate pattern
```bash
rm *ate*
```

# Question mark ?

- list every file that follow this pattern, where ? stands for any character
```bash
ls l?st.txt
```

- list every file that follow this pattern,  where ? stands for any character
```bash
ls ??st.txt
```


# Bracketed Characters

- list every file which contains in the pattern a word like a or e or f
```bash
ls l[aef]st.txt
```


___
## References
[[LPIC-1 Exam 101.pdf#page=]]