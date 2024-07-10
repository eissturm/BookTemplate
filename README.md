# Andrew Meyer's Book Template
*This is a template repository. Content here is intented to be adapted to your project*

## What is *{Your Book Name}*?
{ provide a short summary of your book or writing project }

## The Process

![workflow diagram](/Workflow%20Diagram.png)

### Write 
The book is written in individual chapter .docx files, stored in the `/Manuscript`directory.

### Table of Contents
Also located in the `/Manuscript` directory, the `toc.yaml` file tracks the order to compile chapters at build time.

### Compilation
The `/Manuscript/build.py` file compiles them, and can be triggered by a Github Action to build the book securely in the cloud.

### Branching
Using git's branching capabilities, we can track and control what versions of the story have been released to our collaborators and our readers.

| Branch | Purpose | Audience |
| ------ | ------- | -------- |
| working | track my work as I'm writing it | author |
| nightly | to review holistic state of the book as it is being written/refined | internal collaboration/editorial team |
| alpha | versions of the book that are ready for early feedback and testing | Close family/friends, external editorial/marketing |
| beta | the book is nearing its final form. Now open for wider feedback | Friends/family, trusted fans |
| main | candidates for final publication | publishing staff, advance readers/reviewers |
| release | the finalized, published version of the book | Public |

### Automation
Github Actions power automated compilation of the book when a new contribution is committed to the private repository. The output of these automations is protected and secured to only the author and allowed contributors. Branches `nightly`, `alpha`, `beta`, and `main` are currently configured for auto-build. The `nightly` branch is caught up to the `working` branch every night at 9pm.

When configuring this for your own environment, modify the `.github/workflows/build-manuscript.yml` to have your book's name where referenced between the `{ }` symbols.

### Statistics
The `/Stats` directory contains a jupyter notebook that processes the build and performs statistical analysis and trending of my progress.

### Private Notes
`/Notes` contains plot, setting, and character notes relevant to the writing process, but not directly part of the manuscript.

## Why
> Why do this? Previously, I had been writing in one big file because I found that compiling things manually at scale was tedious. However, this meant that cross referencing parts of the book often became difficult, and historically my drafts can drift significantly during the writing.  Switching to writing in individual documents fits my desired workflow more completely, and being able to automatically build it into a "complete" document is really quite slick. I can now have multiple parts of the book side by side to ensure that they are self-consistent.

> The branching allows me to control more easily track what the story is and what people have read as I am writing and evolving it.
> - Andrew Meyer