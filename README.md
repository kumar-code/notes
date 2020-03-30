# Notes

# Git Commands
Git push rejected “non-fast-forward”

It looks, that someone pushed new commits between your last git fetch and git push. In this case you need to repeat your steps and rebase feature_branch one more time.

1. git fetch
2. git rebase remote_name/feature_branch
3. git push origin remote_name/feature_branch

After the git fetch I recommend to examine situation with gitk --all.
