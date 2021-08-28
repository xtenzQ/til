# Interface based programming

Just read this term in the book "Think Data Structures" by O'Reilly and decided to google it a bit.

> It's a matter of expressing dependencies in terms of interfaces instead of concrete classes

In other words:
- You can write your code before implementing the real dependency;
- You can test via mocking really easily (without having to mock classes, which gets ugly);
- It's clear what you depend on in terms of the API instead of implementation (i.e. you have looser coupling).

[Answer from Jon Skeet](https://stackoverflow.com/a/1848486)
