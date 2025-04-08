# Deleted Origin Branches Not Removed
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
[https://stackoverflow.com/questions/15289768/github-commits-arent-recorded-in-the-your-contributions-calendar
