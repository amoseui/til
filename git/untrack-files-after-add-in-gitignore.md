# Untrack files after add in .gitignore

Add some files you don't want to track anymore in .gitignore in the middle of the project

.gitignore
```bash
gradle.properties
```

---

```bash
$ git add .gitignore
$ git commit -m "test"
$ git rm --cached -r gradle.properties
$ git status
On branch master
Changes to be committed:
  (Use "git reset HEAD <file>..." to unstage)
      deleted: gradle.properties

$ git add gradle.properties
$ git commit --amend
```


Now the file is not in the version control and still alive in local.
