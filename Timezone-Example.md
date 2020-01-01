committed at `2020-01-01T10:00:00+0000` <- this is equal to the next
committed at `2020-01-01T06:00:00+0400` <- this is equal to the previous
committed at `2020-01-01T10:00:00+0200` <- this is two hours later


Variations of this command were used to make the commit:
```
GIT_COMMITTER_DATE="2020-01-01T10:00:00+0000" GIT_AUTHOR_DATE="$GIT_COMMITTER_DATE" git commit -m "Timezone example. $GIT_AUTHOR_DATE."
```
