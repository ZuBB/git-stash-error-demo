### possible git bug

### STR
* copy new over old
* run `git stash -p`
* choose `s` to go with each chunk separately
* say `y` to all chunks
* observe output for the last one

#### Results
- *expected result*: no error happened, all changes have been stashed;
- *actual result*: adding last chunk fails with next error

```
error: patch failed: static/scss/results-widgets/match-as-progress.scss:3
error: static/scss/results-widgets/match-as-progress.scss: patch does not apply
error: 'git apply' failed
```

#### Note

If we say `a` to whole file in STR at step #3, all also ends without a glitch

### Answer

https://stackoverflow.com/a/12763901/1344249
