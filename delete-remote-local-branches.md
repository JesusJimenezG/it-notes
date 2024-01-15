# Delete branches locally and remotely

## Delete local branch

```bash
git branch -D <branch_name>
```

## Delete remote branch

```bash
git push -d <remote_name> <branchname>
```

Note: Don't forget to do a `git fetch --all --prune` on other machines after deleting the remote branch on the server.

Source: [StackOverflow](https://stackoverflow.com/a/2003515)
