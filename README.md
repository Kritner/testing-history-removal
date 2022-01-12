# Testing History Removal

This change is being done in original commit 1 with a mod in original commit 2

this change is in original commit 2

more updates.

This is a feature branch doots! we're doing some doots!

This is one final commit to the repo before attempting to rewrite history.
Right now looking at history, you'll be able to see all changes to the repo over time... including to files that no longer exist in the repo.

This intention of the rebasing is to attempt to take a situation like...

```
commit[0] ... commit[1] ... commit[50] ... commit[n-1]
```

and rewrite history such that `commit[0] ... commit[50]` (as an example) become a single new `commit[0]`, where all changes between the original `commit[0]` and `commit[50]` are "squashed" into the new `commit[0]`.

Doing such a change will of course change the commit hashes *after* the original `commit[50] ... commit[n-1]`, which has the issue of existing tags no longer referring to a valid commit point in history.
