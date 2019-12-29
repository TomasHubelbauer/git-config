# Git configuration

[**WEB**](https://tomashubelbauer.github.io/git-config)

My preferred Git configuration.

```
git config --global user.email "tomas@hubelbauer.net"
git config --global user.name "Tomas Hubelbauer"
git config --global pull.ff only
git config --global merge.ff only
```

`pull.ff` causes non-fast-forward merges (the ones that would create a merge commit when doing `git pull`) to error
instead of creating a merge commit. This means that if I forget to run `git pull --ff-only` I will be reminded to do
that with that error instead of getting a merge commit which I would have to undo then. Of course most of the time
I (or my IDE) am actually doing `git pull --rebase` so this is for when I zone out while using the CLI to pull.

I am not sure if `merge.ff` is redundant here or not so I put it in just in case because it is faster than testing it.

## To-Do
