# Delete Origin Branches No Longer in Repo
There are some git branches in a repo that is deleted by still appearing in origin.

## Root Cause
```git fetch``` does not remove origin branches that is deleted.

## Resolution
1. Go to the location of the repo.
2. Type the following repo to remove all deleted branches.
```
git branch -vv | grep 'gone]' | awk '{print $1}' | xargs git branch -D
```

## Reference
https://www.reddit.com/r/git/comments/hgronz/delete_local_branches_that_do_not_have_remote/
