# Code Review Checklist
A guide for reviewing code and having your code reviewed.

> <i>Given enough eyeballs, all bugs are shallow.</i>
>
> <cite>Linus' Law</cite>


**Remember, the purposes of a code review are:**

1. To improve the quality of the software
2. To *document* that we have improved the quality of the software
3. To improve the knowledge and skill of *the reviewer*, as well as the
   author.

## Table of Contents

* Code Review Best Practice
    * Everyone
    * Having Your Code Reviewed
    * Reviewing Code

* Checklist
    * Correctness
    * Testing
    * Documentation
    * Error Handling and Logging
    * Design
----

## Code Review Best Practice

> <i>Criticism may not be agreeable, but it is necessary. It fulfils the same
> function as pain in the human body. It calls attention to an unhealthy state
> of things.</i>
>
> <cite>Winston Churchill</cite>

### Everyone

* Accept that many programming decisions are opinions. Discuss tradeoffs, which you prefer, and reach a resolution quickly.
* Ask good questions; don't make demands. ("What do you think about naming this :user_id?")
* Good questions avoid judgment and avoid assumptions about the author's perspective.
* Ask for clarification. ("I didn't understand. Can you clarify?")
* Avoid selective ownership of code. ("mine", "not mine", "yours")
* Avoid using terms that could be seen as referring to personal traits. ("dumb", "stupid"). Assume everyone is intelligent and well-meaning.
* Be explicit. Remember people don't always understand your intentions online.
* Be humble. ("I'm not sure - let's look it up.")
* Don't use hyperbole or sarcasm. ("always", "never", "endlessly", "nothing")
* Keep it real. If emoji, animated gifs, or humor aren't you, don't force them. If they are, use them with aplomb.
* Talk synchronously (e.g. chat, screensharing, in person) if there are too many "I didn't understand" or "Alternative solution:" comments. Post a follow-up comment summarizing the discussion.

### Having Your Code Reviewed

 * Be grateful for the reviewer's suggestions. ("Good call. I'll make that change.")
 * Don't take it personally. The review is of the code, not you.
 * Explain why the code exists. ("It's like that because of these reasons. Would it be more clear if I rename this class/file/method/variable?")
 * Push commits based on feedback as isolated commits to the branch. Reviewers should be able to read individual updates based on their feedback.
 * Seek to understand the reviewer's perspective.
 * Try to respond to every comment.

### Reviewing Code
 * Communicate which ideas you feel strongly about and those you don't.
 * Identify ways to simplify the code while still solving the problem.
 * If discussions turn too philosophical or academic, move the discussion offline. In the meantime, let the author make the final decision on alternative implementations.
 * Offer alternative implementations, but assume the author already considered them.
 * Seek to understand the author's perspective.
 * Sign off on the pull request with a :+1: `:+1:` or "Ready to merge" comment.
 
---- 
## Checklist


### Correctness

> <i>Correctness is clearly the prime quality. If a system does not do what it is
> supposed to do, then everything else about it matters little.</i>
>
> <cite>Bertrand Meyer</cite>

#### Does the program do what it's supposed to do?

- [ ] Is the output correct?
- [ ] Are there circumstances under which the program will give the wrong output?
- [ ]  What assumptions does the program make about input?


### Testing

> <i>[T]esting is not a phase to be performed after development is complete. It
> needs to be done all the time throughout the delivery process by everybody[.]</i>
>
> <cite>Jez Humble</cite>


#### Has the program been tested?

- [ ] Are there unit tests available?
  - [ ] Do the unit tests cover all the important functionality of the program?
- [ ] If we have to change some part of the program, how will we know that the
  rest of it still works correctly?


### Documentation

> <i>Incorrect documentation is often worse than no documentation.</i>
>
> <cite>Bertrand Meyer</cite>

#### Will developers be able to understand how to modify the program?
* How is the functionality of the program documented?

- [ ] Is the documentation accurate?
- [ ] Is the documentation easy to understand?
- [ ] Is all of the documentation contained in the source code?

#### Will users be able to understand how to run the program?

 - [ ] Is there a usage message? 
   - [ ] Is it accurate? 
   - [ ] Is it helpful?
 - [ ] Is the rest of the user-side documentation accurate?
 - [ ] Is there enough user-side documentation?


### Error Handling and Logging
#### What happens when something goes wrong?

* Under what circumstances will the program fail to run?
- [ ] Are the error message informative?
- [ ] In cases of user-error, does the user get adequate information about what he
  or she did wrong?
- [ ] Does the program produce a reasonable amount of logging for its function?


### Design

> <i>[D]o not let performance considerations stop you from doing what is right.
> You can always make the code faster with a little cleverness. You can
> rarely recover so easily from a bad design.</i>
>
> <cite>Elliotte Rusty Harold</cite>

#### Is the program flexible?

- [ ] Will developers be able to modify the program to fit changing requirements?
- [ ] Are there hard-coded data that should be modifiable?
- [ ] Is the program sufficiently modular? Will modifications to one part of the
  program require modifications to others?

#### Could the program be simpler?

- [ ] Do you, the reviewer, understand what the code does?
- [ ] Does the program reinvent the wheel?
   - [ ] Can parts of the functionality be replaced with the standard library?
   - [ ] Is there redundant functionality in two different programs?
- [ ] Is all of the functionality necessary? Could parts be removed without
  changing the performance?
- [ ] Is the code commented?
   - [ ] Are the comments necessary?
   - [ ] Could the code be rewritten so that the comments aren't necessary?

#### Is the code readable?

- [ ] Is the code formatted according to the conventions of the language?
- [ ] Are the formatting conventions consistent?
- [ ] Are the variable names reasonable?


[QMS_info]: http://gin.bcgsc.ca/plone/groups/quality/bioinformatics-quality-assurance/documents
[Whitepaper]: http://gin.bcgsc.ca/jira/secure/attachment/32569/WP-CC-11-Best-Practices-of-Peer-Code-Review.pdf
