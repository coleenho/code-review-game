---
layout: default
---

# The Author
Long before a code review takes place, there are certain things that can set it up for success:  
1. **Make small changes**: Make code changes as small as possible.  No one wants to be invited to a code review with 20 or more files that include over 400 lines of code that were modified.  Plan code changes in incremental chunks.  This makes the review process run smoother and quicker because there are smaller bite size bits of code (no pun intended) to digest.  It will also make it easier to find any potential issues.
2. **Set context**: Describe the changes being made and *why*.  This can be done in the code itself, technical documentation, description in the code changelist, or in a ticket system. It also provides traceability; months or years from now someone can understand why this change was put in place.
3. **Establish quality**: Ensure the code builds, tests pass, and code coverage is at an acceptable level.  Fixing a bug?  Make sure that tests are added to cover the fix that is implemented.  No tests exist at all?  Then be the first to add a test; it’s gotta start sometime and it will make the code base all the more stronger!

Once the code is ready to be reviewed, follow the guidelines below to proceed through the phases of the code review.

## Code Review Guidelines
The code review process includes three distinct phases: before, during, and after code review.  Each phase includes several key aspects and optional checklists to ensure a successful and productive code review occurs.  I’ve learned and discovered many of these aspects through my own experience as The Author of code reviews.  My aim is to make the review process as easy for my Reviewer as possible.  This is accomplished through preparation on my side as The Author.

### Phase 1: Before Code Review
In order to promote a successful code review, prepare yourself and The Reviewer by establishing the context for the changes, ensuring the code quality is maintained, and the appropriate format for the review is established before the code review begins.

#### Context
A description establishes context and provides the necessity for the change being introduced.  State the case for modifying this code–imagine someone asks, “Why is this code changing?”  This answer should be provided to the Reviewer.

#### Code Quality
Verify the code compiles/builds and runs.  All tests should pass and meet code coverage goals to ensure the quality of the code is maintained and enhanced.  In order to demonstrate the scope of the changes as well as a continued enforcement of those changes, tests should be added/modified as necessary.  This helps ensure the code will continue to work as expected despite changes that may occur around it.

#### Reviewers and Review Format
It is usually better to include more reviewers than fewer depending on the scope of the review.  This allows flexibility within the team to decide who is reviewing the code and when.  It also broadens awareness of the code changes.  Consider the preferred format (live or offline) for your review.  A live code review has The Author walk The Reviewer through the code changes versus an offline review where The Reviewer reviews the code on their own time without direct interaction with The Author.  See Table 1 below for a comparison between live and offline code reviews to determine the best match for your code review.  Also, consider the option of doing both a live and offline review with The Reviewer.

Table 1: Comparison of Live and Offline code reviews

| | Live | Offline |
| --- | ---- | ------- |
| **Driver of Code Reviewer** | Author | Reviewer |
| **Speed of review** | Possibly Faster | Slower |
| **Depth of scope** | Brief (might miss issues) | Thorough |
| **Changelist size/impact** | Preferred for complex, impactful, or large changes | Best for small, simple changes |

> Note, The Reviewer has the option to request a live code review to clarify any changes.  This helps reduce the back and forth in offline reviews and enhances the review process.

> Do live code reviews if the changes are large, impactful, or complex; offline code reviews are perfect for simple or minimal code changes that don’t require much discussion. 

To ensure preparedness for your review, use the following checklist:

#### Before Review Checklist
- [ ] Provide Description (describe **what** the code change is and **why** it is needed)
- [ ] List use cases and edge cases
- [ ] Ensure code compiles/builds
- [ ] Validate code runs
- [ ] Verify tests pass
- [ ] Add/modify tests to handle the code change
- [ ] Meet code coverage as required by your team
- [ ] Check all common mistakes are avoided (see the Gotchas section)
- [ ] Identify reviewers
- [ ] Decide live or offline review

> If holding a live code review, present the changes in a logical flow.  Suggestions:\
> - APIs, UI, or database level first
> - Data flow
> - Tests first

Once all aspects from the Before Review Checklist above are covered, invite The Reviewer to assess the changes.  Work with The Reviewer to determine when feedback can be expected.  Typically 1-2 days is appropriate for smaller code reviews.

### Phase 2: During Code Review
Don’t take it personally if there are change requests to the code.  The Reviewer has assessed the code and is asking for a rewrite based on their opinion.  Any change request should be discussed with The Reviewer when there is disagreement or it is unclear.  This becomes an excellent learning opportunity!

This was a vital step I learned in the code review process.  Understanding the reason for the rewrite helps you avoid repeating the same mistakes.  Also, with this experience you are able to look out for it in other engineer’s code reviews.  Remember there is room for disagreement, but we need to strive to come to a consensus on what is best for the code base.

> Do your best to set your ego aside.  Come to a code review with an open mind.

### Phase 3: After Code Review
Now evaluate how your code reviews are going.  Are there improvements?  If not, work to identify The Gotchas before the next code review.  Seek out counsel from other engineers before and during coding.  Try to improve your own personal code review score.  Keep in mind, this is a measurement you define, not one that would be assessed from any of The Reviewers.  Look at the following checklist for items to conclude your review:

#### After Review Checklist
- [ ] Identify your own list of Gotchas
- [ ] Strive to avoid these mistakes in your future code reviews 
- [ ] Be sure to reciprocate and review code changes from your Reviewers
- [ ] Learned something new

You haven’t won The Game if there are no change requests from your review.  It may mean you should seek more challenging problems.  Try extending yourself in another direction–contribute to another teams’ work or code something for the front end if you are a backend developer.  Find new ways to play The Game–don’t limit yourself to just one.

Not confident being a Reviewer quite yet?  Try these:
1. **Watch**: Shadow experienced reviewers on your team to watch and learn. 
2. **Practice it**: Be encouraged to take the risk and review code regardless of your career level.
3. **Teach others**: Show how to identify issues in other engineer’s code to avoid making those mistakes in your own code.

Utilize the list of Gotchas to identify areas in the code you are comfortable reviewing.  Then challenge yourself and pick one or two Gotchas you aren’t as familiar with and practice reviewing with those in mind so you can grow your reviewing and coding skill.
