---
title: "Cloud Based Online Compiler"
date: 2024-01-15
draft: false
featured: true
thumbnail: "/thumbnails/maple.png"
description: "An online compiler supporting multiple C/C++ compiler versions with code isolation using AWS Lambda for secure execution."
technologies: ["Python", "AWS Lambda", "Docker", "C/C++", "React"]
github: "https://github.com/roblee04/online-compiler"
demo: "https://youtu.be/PM6lQ51qowQ"
status: "Completed"
---

## Cloud Based Online Compiler

An online compiler built to support a variety of compiler versions (and in the future, runtime environments/libraries) for C and C++ code.

### Key Challenge

The most frightening part about the project was how to do **code isolation** - executing untrusted user code securely. This problem was solved using **AWS Lambda**, which provides isolated execution environments.

### Features

- Multiple C/C++ compiler versions supported
- Secure code execution via AWS Lambda
- Clean web interface for code input/output
- Future support planned for additional languages and libraries

### Demo

[Watch Demo on YouTube →](https://youtu.be/PM6lQ51qowQ)

### Source Code

[View on GitHub →](https://github.com/roblee04/online-compiler)