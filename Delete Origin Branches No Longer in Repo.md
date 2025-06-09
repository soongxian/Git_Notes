# Delete Origin Branches No Longer in Repo
There are some git branches in a repo that is deleted by still appearing in origin.

## Root Cause
```git fetch``` does not remove origin branches that is deleted.

## Resolution
1. Go to the location of the repo.
2. Type the following repo to remove all deleted branches.
```
git remote prune origin
```

## Reference
https://www.reddit.com/r/git/comments/1c9ulfi/how_do_i_delete_remote_branches_in_local_git_repo/?rdt=41755
