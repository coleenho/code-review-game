---
layout: default
---

# The Reviewer
Being part of a code review should be viewed as a privilege, not a burden.  It says The Author values your input and feels you have something worthwhile to contribute–these requests should be taken seriously. Try to offer suggestions, but also realize that a lot of work went into The Authors’ changes.

> Challenge yourself to provide positive comments in a code review.

Prepare yourself for the code review.  Set aside 10-60 minutes for the review and preferably as soon as you are invited to provide timely feedback.  For a live code review, be sure to look at all the changes beforehand so you can bring your questions to the meeting.  For both live and offline reviews, follow the checklist below to prepare yourself and identify common mistakes (see the Gotchas section near the end of the paper).

## Code Review Guidelines
Just as The Author has three phases of the code review process, so does The Reviewer: before, during, and after code review.  Unlike The Author, The Reviewer will spend most of their time in Phase 2.  Phase 1 is still important, however, because it helps The Reviewer determine the readiness and plan for the code review.

### Phase 1: Before Code Review
Assess the code review request.  Be sure to ask The Author for anything you may need: context and additional Reviewers.  Collaborate with other Reviewers to discuss an approach for the code review.

If significant change requests occur during an offline review, then hold a live code review to discuss any concerns.  Conducting a live review will streamline the process and clear up misunderstandings on either side.  This prevents frustrations and other negative interactions.

This flexibility in the format for a code review is important.  I’ve seen many code reviews where a live setting would result in less time writing feedback and thus conclude earlier.  For example, when something is unclear to me or I have more than 5 change requests, I will ask for a live code review to have a collaborative working session.

For large code reviews, consider dividing and conquering with the other reviewers.  One way is to divide the files to be reviewed and another way is to divide the Gotchas across all changes.  Reduce the redundancy of code reviews just like you would reduce the redundancies in code.

When you are ready to proceed with the code review, step through this checklist to make sure you are prepared:

#### Before Review Checklist
- [ ] Review description (understand what and why this change is needed)
- [ ] Understand the requirements
- [ ] Identify use cases and edge cases for potential defects
- [ ] Ensure code compiles/builds
- [ ] Check code runs
- [ ] Make sure tests pass
- [ ] Verify tests are added/modified to handle the code change
- [ ] Confirm team’s code coverage standard is reached
- [ ] Identify your scope for the review
- [ ] Prepare 10-60 minutes for the review (based on the size of the code changes)

> Exceeding 60 minutes may be a red flag that the code review is too big or the requirements are unclear.

### Phase 2: During Code Review
Think of code reviews as the same process as writers go through with editors.  It’s not about criticizing how or what The Author wrote.  This is a time to be constructive–offer suggestions for improvement as much as possible and provide justification.  Don’t just simply identify what the issue is.  Be respectful with your feedback; focus on the problem and not The Author.

For example, take these lines of code under review:
```
for (int i = 0; i < n - 1; i++) {
    for (int j = 0; j < n - i - 1; j++) {
        if (arr[j] > arr[j + 1]) {
            // swap arr[j+1] and arr[j]
            int temp = arr[j];
            arr[j] = arr[j + 1];
            arr[j + 1] = temp;
        }
    }
}
```
This is an example of the Bubble Sort.  It is a brute force approach for sorting an array and is generally not preferred due to its O(n<sup>2</sup>) time complexity.  The Reviewer may not recognize this algorithm, but they might notice the use of the inner for loop.  Let’s look at possible feedback for this code.

One concern may be the performance implications.  Simply stating “This change will destroy performance!” is an example of hyperbole and should be avoided.   Instead, confirm with The Author that their change is intentional.  For example, “It seems like this might be a slower solution.  Do you intend to have a double nested for loop?”.  This will guide The Author through your feedback and provide them with something tangible to address.  Furthermore, notice your tone and language in your feedback.  Try to avoid phrases like “obviously” and “why did you do this?”.  This can lead to adversarial reviews and cause people to feel defensive or hurt.

Also, be mindful of the severity of the change requests.  If something isn’t critical, call it out as a nit (as in nitpick).  This signals that it isn’t necessary to modify, but it is more suggestion based like an opinion: “Nit: can you change the variable name from ‘dt’ to ‘dailyTotal’ to make it clearer what it’s for?”.

It’s important to convey why a change request is warranted.  The Author has given their best solution so it is vital you provide recommendations along with justifications.

> Provide recommendations with justification, not just feedback.

Don’t get distracted by things other than the actual changes The Author made.  If you notice something else outside the review at hand, take note and handle that independently.  Keep the review on track and short–this is especially important during live code reviews when you engage with other engineers.  If you get hung up on something, take note to discuss offline and move on.  If a solution to a change request cannot be reached immediately, discuss this offline as well.

Along with minimizing distractions, consider the following:

#### Outside the Scope of Code Reviews
- Code that hasn’t been modified.  If there’s an issue beyond The Author’s change, create a ticket for it.
- Architectural or design discussions should be addressed in a separate meeting.  However, stop the code review if those discussions may change the code that is being reviewed.
- Personal preferences when it comes to coding style.  Refer to actual deviations from coding standards for your team/company.

Use the following checklist to guide you through the reviewing portion:

#### During Review Checklist
- [ ] Consider all possible cases (happy paths and sad paths)
- [ ] State assumptions and where changes might break
- [ ] Focus on new code and confirm it fulfills requirements
- [ ] Identify exceptional cases and whether they are handled and tested
- [ ] Utilize language specific features
- [ ] Give positive and constructive feedback
- [ ] Check the Gotchas list for common mistakes

#### Phase 3: After Code Review
To conclude the code review, ensure The Author and other Reviewers know you are finished.  Proceed with this checklist to wrap up your portion of the review process:

#### After Review Checklist
- [ ] Follow up with The Author
- [ ] Confirm feedback is understood
- [ ] Read feedback from other Reviewers
