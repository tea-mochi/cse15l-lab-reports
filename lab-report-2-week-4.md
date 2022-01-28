# Week 4 Lab Report -

## Example 1 - during week 3

![Image](report-2\4.png)
[noLinkFile.md](https://github.com/tea-mochi/markdown-parse/blob/main/noLinkFile.md?plain=1)
![Image](report-2\5.png)

When MarkdownParse was run with failure-inducing input `noLinkFile.md`, the symptom shown was throwing an index out of bounds exception. The bug was that the program tried to return a section of code by calling substring on other fields–`openParen` and `closeParen`–which could be -1 if parentheses did not appear in the file. To fix this, we `return;` from main when any of `(` , `)` , `[` , `]` don't appear in (the rest of) the file.

---

## Example 2 - during week 3

![Image](report-2\7.png)
[fakeLink.md](https://github.com/tea-mochi/markdown-parse/blob/main/fakeLink.md?plain=1)

![Image](report-2\6.png)

When passing failure-inducing input `fakeLink.md` as the arg to MarkdownParse, the symptom shown was that it returned `[also known as felis catus]` when expecting `[]`. The bug that led to this symptom was that we didn't check that link syntax was in the proper spacing/order. To fix this, we added a check to make sure there were no spaces between `)` and `[`, i.e. `[text](text)`.

---

## Example 3 - during week 4

![Image](report-2\1.png)
![Image](report-2\2.png)
The 7 files not shown are the addition of test files 2-8, I only made one commit for all these because only [testfile-8.md](https://github.com/tea-mochi/markdown-parse-main/blob/main/test-file8.md?plain=1) contained a failure-inducing input.

![Image](report-2\3.png)

When failure-inducing input `test-file8.md` was passed as the argument for MarkdownParse, this produced the symptom printing `[a link on the first line]` when we expected `[]`. The bug that caused this was that the code didn't catch situations where the proper syntax was used `[something](link)` but the "link" section contained a space which made it invalid.