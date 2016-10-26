# Update a new post

Update a new post and deploy it to blog.

---

Create a draft.

```bash
$ hexo new draft ${title}
```

in source/_drafts/${title}.md

```markdown
---
title: ${title}
tags:
  - tag
---

contents
```
---
Publish a post in draft

```bash
$ hexo publish draft ${title}
```
---
Generate and run server
```bash
$ hexo generate
$ hexo server
```
---
