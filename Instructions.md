# Instructions for Using Quiz Templates

## Introduction

This document describes the required structure for GitHub repos for quizzes.
Quiz repos that are laid out correctly can be used to update the quiz in Canvas
using the `github-to-canvas-quiz` gem. (See the [gem's
instructions](https://github.com/learn-co-curriculum/github-to-canvas-quiz) for
how to do that.) The formatting and structure of the files must follow the
examples shown here exactly in order to update correctly (with the exception of
some metadata that is optional - see info below).

In addition to these instructions, the `canvas-quiz` folder in this repo
provides templates/examples for the required components.

## Quiz Repo Structure

The quiz repo consists of a `README.md` file and a `questions` folder.

### README file

The `README.md` file contains:

- some metadata about the quiz
- the quiz title
- the student-facing general instructions for the quiz

The `README.md` file in this folder can be used as a template. Here's an example
of a completed `README.md` file:

```text
---
id: 20131
course_id: 3299
repo: phase-3-quiz-arrays-and-hashes
---

# Arrays and Hashes Quiz

It's time to check your knowledge! Use this quiz to create a custom study guide.
Note any answers that were marked incorrect, so you can study the relevant
material and try this quiz again.

If you don't know the answer to a question, please do not guess. Instead, select
"I don't know". It's OK not to know everything and to admit when we're unsure.
```

### Questions Folder

The `questions` folder contains one file per question. The naming convention for
the files is: `00.md`, `01.md`, etc.

### Questions Files

Each question file contains:

- metadata about the quiz question
- The content of the question itself, including:
  - The title of the question
  - The question text
  - Correct and incorrect responses. What these look like varies according to
    the question type.

See the question files in the `questions` folder for templates to set up
the different types of questions that can be used in Canvas:

- `00.md`: [short answer][] (called "Fill in the Blank" in Canvas)
- `01.md`: [multiple choice][]
- `02.md`: [multiple answers][] (i.e., select all that apply)
- `03.md`: [true/false][]
- `04.md`: [matching][]
- `05.md`: [multiple dropdowns][]
- `06.md`: [fill in multiple blanks][]

Each of the question types listed above links to an example in GitHub.

### Required and Optional Metadata

README: all metadata is required.

**Note**: in theory, if the `id` (which represents the quiz id) is omitted, the
gem will create the quiz and fill in the `id` returned by Canvas. **However**,
this functionality is currently broken - running `github-to-canvas-quiz align`
returns a `404 Not Found (RestClient::NotFound)` error. I have not had a chance
to investigate this issue.

Question files:

- `id` (the question id) is required if the question already exists in Canvas.
  If it is omitted, the question will be created and its `id` will be
  automatically populated in the `##.md` file.
- `sources` is optional

[short answer]: https://learning.flatironschool.com/courses/3297/quizzes/22405/take?preview=1
[multiple choice]: https://learning.flatironschool.com/courses/3297/quizzes/22405/take/questions/146235?preview=true
[multiple answers]: https://learning.flatironschool.com/courses/3299/quizzes/20131/take/questions/130250?preview=true
[true/false]: https://learning.flatironschool.com/courses/3297/quizzes/31701/take/questions/210218?preview=true
[matching]: https://learning.flatironschool.com/courses/3264/quizzes/18300/take/questions/124109?preview=true
[multiple dropdowns]: https://learning.flatironschool.com/courses/3299/quizzes/19086/take/questions/120510?preview=true
[fill in multiple blanks]: https://learning.flatironschool.com/courses/3299/quizzes/19094/take/questions/149618?preview=true
