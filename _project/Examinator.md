---
title: "Examinator 🧐"
excerpt: "Unauthorized collaboration detection at scale for online exams. <br/><img src='/images/Examinator-timestamps-chart.png' width='200' height='100'>"
collection: project
date: 2024-03-09
---

Examinator is a secret tool that I built to detect cheating in online exams and homework at scale for large courses with 1000+ students 😉. I built it by reverse engineering Canvas New Quizzes network traffic to scrape students responses as well as activity timestamps.

- During Fall 2023, we caught 3.5% (35 out of 1000) students.
- During Spring 2023, we caught 5% (~70 out of 1300) students.
- During Fall 2022, we caught 13% (11 out of 82) students cheating in the midterm and final exam of an in-person undergraduate CS course.
- During 2021, we caught 20 students cheating in the midterm and final exam of a graduate CS course.

We have a paper published [Examinator v3.0: Cheating Detection in Online Take-Home Exams](https://dl.acm.org/doi/10.1145/3573051.3596196), [Examinator v4.0 : Cheating Detection in Online Take-Home Exams]([text](https://dl.acm.org/doi/10.1145/3657604.3664659)), and a patent pending.

Examinator started as [a research project at Georgia Tech since 2021](https://gvu.gatech.edu/research/projects/examinator-plagiarism-detection-tool-take-home-exams).

We are still actively iterating on the project and expanding 

![Examinator Activities Timestamp Chart](/images/Examinator-timestamps-chart.png)