---
layout: default
---

# Gotchas

Gotchas are mistakes that are introduced by code changes from The Author.  These Gotchas are language agnostic and fairly common.  They can be classified according to the amount of effort required to identify them: Easy, Medium, and Hard Gotchas.  Generally, there is a direct correlation between the visibility of the Gotchas and the severity of issues they can cause.

Both The Author and The Reviewer should consider Gotchas as part of the code review process.  Use the identification methods along with typical causes to find Gotchas as illustrated in Table 2.

Table 2: Comparison of Gotchas

|     | Easy | Medium | Hard |
| --- | ---- | ------ | ---- |
| **Identification Methods** | Automation and quick reviews | Detailed and careful reviews | Holistic reviews
| **Typical Causes** | Coding shortcuts | Sloppy coding | Poor planning
| **System Impact** | Maintainability | Defects | Overall performance and quality
| **Resolutions** | Linters, spell checking, code coverage tools, IDEs | Testing | Consider rework or new approach

Unfortunately, Easy Gotchas often obscure the Medium and Hard Gotchas.  Thus it is important to ensure Easy Gotchas are caught before starting code reviews so the higher level issues can be identified.  Consider the list of Gotchas below:

## Easy Gotchas
- Confusing or inappropriate names for variables, methods, classes/interfaces
- Hardcoded values
- Commented out code (just get rid of it, YAGNI)
- Limit imports to include what is needed, not the whole directory/package
- Linting issues
- Not following coding standards
- Deviation from established code style
- Lack of comments in code
- Copy/paste mistakes
- Spelling
- Formatting

> Automate as much of the Easy Gotchas as you can through code review tools, linters, IDEs, etc.

## Medium Gotchas
- Complex logic statements
- Handling exceptions
- Missing logging statements
- Neglecting to handle null, undefined, or empty string cases
- Hacks or work arounds
- Redundancy in code
- Maintainability
- Readability
- Edge cases not covered
- Tightly coupled code
- Requirements not met
- Insufficient use of interfaces
- Unnecessary changes
- Poorly structured code


## Hard Gotchas
- Multithreading issues
- Asynchronous code
- Performance concerns
- Security flaws
- Lack of design pattern utilization
- Architectural issues
- Additional technical debt

> If you uncover more than one Hard Gotcha, do a live code review.

Identify The Gotchas that you missed as a Reviewer or Author.  These should be key areas you need to focus on to grow as a software engineer.
