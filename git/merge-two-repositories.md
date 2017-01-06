# Merge two repositories

e.g.) Merge Android Music repository to my project.

```bash
$ git clone git@github.com:amoseui/android-music-renewal.git
$ git remote add Music https://android.googlesource.com/platform/packages/apps/Music
$ git fetch Music
$ git merge --allow-unrelated-histories Music/master
$ git remote remove Music
$ git log --oneline
5c0ac48 Merge https://android.googlesource.com/platform/packages/apps/Music
51bfd7f Initial commit
ef3044c Import translations. DO NOT MERGE
291eb7c Import translations. DO NOT MERGE am: 46bf87f2b7  -s ours am: 83ccd60392  -s ours am: 38bd4e8a77  -s ours
```
