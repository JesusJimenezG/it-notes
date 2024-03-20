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

## Delete local branches that have been deleted remotely

```bash
git fetch -p ; git branch -r | awk '{print $1}' | egrep -v -f /dev/fd/0 <(git branch -vv | grep origin) | awk '{print $1}' | xargs git branch -d
```

Source: [StackOverflow](https://stackoverflow.com/a/17029936/13784272)
