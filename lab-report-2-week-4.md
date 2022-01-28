# Lab Report 2

## Error 1 : "test-file4.md"

![image](https://myang25.github.io/cse15l-lab-reports/lab2-pictures/lab2-commit1.png)

This was the first set of changes made to the code in order to correct the output when MarkdownParse.java was ran on test-file4.md. The original code would return the following errors when ```java MarkdownParse test-file4.md``` was executed:

This is the markdown file, test-file4.md: [test-file4.md](https://github.com/ucsd-cse15l-w22/markdown-parse/blob/main/test-file4.md)

![image](https://myang25.github.io/cse15l-lab-reports/lab2-pictures/lab2-error1.png)

The bug is in the following lines of code:

```int openParen = markdown.indexOf("(", nextCloseBracket);```

```int closeParen = markdown.indexOf(")", openParen);```

```toReturn.add(markdown.substring(openParen + 1, closeParen));```

The bug causes the variables openParen and closeParen to both be -1. This is because test-file4.md has "[]", but no parenthesis behind it. Therefore, when the index of "(" and ")" are looked for, nothing can be found. The symptom is a StringIndexOutOfBoundsException. When the add method is called, the substring searched for is from index 0 to -1, which throws a StringIndexOutOfBoundsException.


## Error 2 : "test-file5.md"

![image](https://myang25.github.io/cse15l-lab-reports/lab2-pictures/lab2-commit2.png)

This was the first set of changes made to the code in order to correct the output when MarkdownParse.java was ran on test-file5.md. The original code would return the following errors when ```java MarkdownParse test-file5.md``` was executed:

This is the markdown file, test-file5.md: [test-file5.md](https://github.com/ucsd-cse15l-w22/markdown-parse/blob/main/test-file5.md)

![image](https://myang25.github.io/cse15l-lab-reports/lab2-pictures/lab2-error2.png)

The bug is a lack of code that checks if the open parenthesis is right after the closed bracket.

The bug causes add method to work properly, but adds everything that happens to be in parenthesis. This is because test-file5.md has brackets, some random text in between, and some parenthesis with content later in the file. The symptom is a wrong output that is not  a valid link. So far, MarkdownParse.java has no way of testing if "(" is directly after "]". By adding a if statement in the while loop, we can test to see if the index of openParen is 1 more than nextCloseBracket.

## Error 3 : "test-file6.md"

![image](https://myang25.github.io/cse15l-lab-reports/lab2-pictures/lab2-commit3.png)

This was the first set of changes made to the code in order to correct the output when MarkdownParse.java was ran on test-file6.md. The original code would return the following errors when ```java MarkdownParse test-file6.md``` was executed:

This is the markdown file, test-file6.md: [test-file6.md](https://github.com/ucsd-cse15l-w22/markdown-parse/blob/main/test-file6.md)

![image](https://myang25.github.io/cse15l-lab-reports/lab2-pictures/lab2-error3.png)

