---
layout: default
title: Gotchas
---

## Gotchas

### Easy Gotchas
- Confusing or inappropriate names for variables, methods, classes/interfaces
- Hardcoded values
- Commented out code (just get rid of it, YAGNI)
- Imports (only include what you need, not the whole directory/package)
- Linting issues
- Not following Coding Standards
- Different Code Style
- Lack of comments in code
- Copy/paste mistakes
- Spelling
- Formatting

> Automate as much of the Easy Gotchas as you can through code review tools, linters, IDEs, etc.

### Medium Gotchas
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
- Minimal to no use of interfaces
- Extraneous, unnecessary changes
- Poorly structured code

### Hard Gotchas
- Multithreading issues
- Asynchronous code
- Performance concerns
- Lack of design pattern utilization
- Architectural issues
- Additional technical debt

> If you uncover more than one Hard Gotcha, do a live code review.
