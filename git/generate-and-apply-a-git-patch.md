# Generate and apply a git patch

Generate the patch of the topmost <n> commits from a specific <SHA1> hash.

```bash
$ git format-patch -<n> <SHA1>
```
---

Apply the patch file in a local directory.

```bash
$ git apply {NAME}.patch
```
