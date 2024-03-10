---
title: "Jack Marker 🧑‍💻"
excerpt: "Invisible characters after comments (hidden in VSCode, PyCharm, etc). <br/><img src='/images/jackmarker-template-code.png' width='400' height='200'> <img src='/images/jackmarker-hexdump-of-the-first-few-lines.png' width='400' height='200'>"
collection: project
date: 2023-10-09
---

Jack Marker is a tool that me and our lab developed to catch students copied each other's coding homework. Instead of me explaining how it works, it would be more fun for you to read what students said about us in a Reddit post: [Secret CS 3600 (Intro to AI) Anti-plagiarism Trick](https://www.reddit.com/r/gatech/comments/11cofz3/secret_cs_3600_intro_to_ai_antiplagiarism_trick/)


<blockquote>
<h3>r/gatech - Secret CS 3600 (Intro to AI) Anti-plagiarism Trick</h3>
TL;DR: Invisible characters after comments (hidden in VSCode, PyCharm, etc)
<br>
The latest CS 3600 assignment was distributed differently from the previous ones. Every student was assigned their own repository, each with seemingly identical content. A provided reason behind this decision was that students sometimes accidentally create public repositories. Presumably, if they created private repositories for us, that wouldn't be an issue.
<br>
But that was not the actual purpose of per-student repositories (at least, not the entire purpose). Throughout the template is a number of comments: from TODOs that students are meant to delete, to labels over groups of imports. These comments look normal in most editors and IDEs:
<br>
<img src='/images/jackmarker-template-code.png'>
<figcaption>Screenshot of submission template</figcaption>
<br>
The editing experience around these comments also feels normal: walking over them with arrow keys works perfectly fine, and within vanilla VSCode, there is no way to notice anything strange. However, if we look at the raw data in the file, we discover that every single comment ends with Unicode carefully constructed using Latin-1 control codes to be invisible:
<br>
<img src='/images/jackmarker-hexdump-of-the-first-few-lines.png'>
<figcaption>Hexdump of the first few lines</figcaption>
<br>
The comment appears to be `# pgmpy` but there are >40 bytes before the next line begins! Essentially, each student's template includes different invisible characters after every comment. The encoding scheme allows the instructors to include enough data to uniquely identify students based on comments left in the source code. If a student shares code—and the code includes a comment from the template—then the plagiarism can be detected.
</blockquote>