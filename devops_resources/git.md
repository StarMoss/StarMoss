# Git and GitHub Notes

## Workflow
  
`git checkout dev` (checkout the dev branch)

`git pull origin dev` (pull latest changes from the remote dev branch)

`git checkout -b “BRANCH_NAME”` (create your feature branch)

`code .` (Open vs code)

`git add` . (Stage your commits)

`git commit -m "BRANCH_NAME” -m “Descriptive message for the commit.”`

`git push origin BRANCH_NAME`

## Rebase workflow

`git checkout dev`

`git pull origin dev`

`git checkout feature_branch`

`git branch --set-upstream-to=origin/dev [feature branch]` (if it’s not already set)

`git pull --rebase`

`git push origin feature_branch --force`
  
## Rename branch (local)

`git branch -m new-branch-name`

## Delete a branch

`git branch -D branch_name`
  
## Switching contexts with git stash

```
1. Save changes to branch A.
2. Run git stash.
3. Check out branch B.
4. Fix the bug in branch B.
5. Commit and (optionally) push to remote.
6. Check out branch A
7. Run git stash pop to get your stashed changes back.
Git stash stores the changes you made to the working directory locally (inside your project's .git directory; /.git/refs/stash,
```
                                                                        
## Formatting

```
git log --graph --decorate --pretty=oneline --abbrev-commit
git log
git log origin/dev..HEAD
```

----


## Initial Setup

On MacOs, git can be installed using `brew`
                                                                        
```bash
# from your cli
brew install git
```
                                                                        
### Associating SSH Keys with GitHub

- This is a helpful resource when frequently cloning repositories.
- [GitHub SSH Tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

### **Creating a `PAT`**

`Personal Access Tokens` or `PATs` are an essential staple of achieving token-based authentication with `GitHub`.

- [**What is a PAT and why do I need one?**](https://devopsjournal.io/blog/2022/01/03/GitHub-Tokens)
- [**How to generate a PAT**](https://docs.github.com/en/enterprise-server@3.4/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

*Be sure to authorize your PAT for SSO.*

### First-time git setup

Once Git is installed, your Git environment and configuration variables need to be customized with `git config`.

You can view your default Git configuration options with the following command:

`git config -h`

The resulting output should be similar to:

`usage: git config [<options>]`

### Set your git identity

Set your user name and email address. This is important because every Git commit uses this information:

```bash
git config --global user.name "Lindsey Stanton"

git config --global user.email lindseymstanton@gmail.com
```

This only needs to be done once if you include the `–global` option.

After you have set your user name and email address, you can check your settings with the following command:

`git config --list`         

                                                                        






                                                                        

                                                                        
