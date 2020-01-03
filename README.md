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

## Configuring Identity

https://help.github.com/en/github/getting-started-with-github/set-up-git

This article from GitHub is absolute garbage and this is done rarely enough
for me to reliably forget, so here goes:

- Download and configure Git as per the above
- Clone a repository (can be this one for a test)
- Make a change, add it to stage, commit it and push
- Observe a GitHub credential manager pop up
- Enter GitHub username and a PAT (not the password!)
- Enter username and the PAT to the CLI prompt if asked
  (Sometimes the graphical prompt fails after the 2FA step)

Never does it say to use the PAT and not the GitHub account password.
I don't have a problem with the fact that PAT needs to be used, it makes
perfect sense, but unless you already know and remember this, you will be
struggling for a long time! For novices, this must be beyond frustrating
and even for me as an experienced Git user, it still sucks to have to
remember this.

## To-Do
