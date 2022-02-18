## Git error: Encountered 7 file(s) that should have been pointers, but weren't
解决方法：
```
git rm --cached -r .
git reset --hard
git rm .gitattributes
git reset .
git checkout .
```
