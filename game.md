---
layout: default
---

## The Game
A while back I was at a company where I sat near one of the software architects.  I could tell he was really great at his craft, so I frequently sought him out to do my code reviews.  I figured I could learn a lot from him.  My first couple requests for change from my code reviews were incredibly dense; they were detailed, but nit-picky.  I couldn’t believe the amount of things he put in a review; one line of code could easily generate three or more requests for change! 

After a few more reviews, I started improving and getting less requests for change.  For me, it became a challenge; a game of sorts.  I wanted to see whether I could get a code review from this Architect and receive no requests for change.  I turned this initially daunting process into something fun and enjoyable for the first time in my career and I aim to share these best practices with all engineers to improve the code review process.

Consider each role of the code review as a player in the game.  As The Author, the code review is a game consisting of simply trying to improve your own “score” or number of requests for change.  Each code review should see overall requests for change diminish.  For The Reviewer, the game is a little different where their objective is to eliminate leaked defects, improve code quality, and minimize tech debt.  Both players need to ensure the code base is continuously maintained and enhanced but not at the expense of sacrificing quality.  For the game there is not an actual score per say, but you should try to quantify it in some meaningful way for yourself to mark progress as a player.  Examples for keeping score are provided at the end of the page.

Read further on [The Author](author) \| [The Reviewer](reviewer) \| [The Gotchas](gotchas_list)

## Keeping Score
For The Author, use the above lists and count up the number of Easy, Medium, and Hard Gotchas that were caught in the review.  Watch these scores over time to ensure they are improving.

The Reviewer should consider change requests from other Reviewers or leaked defects as part of their score.  Just as The Author keeps score for themself, The Reviewer tracks their own missed Gotchas or leaked defects over time.  This identifies key areas for enhancing the review process.

Through ongoing practice and participation, both players of the code review game aim to achieve better scores.  Ideally, Gotchas and leaked defects no longer occur–which is the ultimate objective of The Game.
