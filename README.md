# Notes

# Git Commands
Git push rejected “non-fast-forward”

It looks, that someone pushed new commits between your last git fetch and git push. In this case you need to repeat your steps and rebase feature_branch one more time.

git fetch
git rebase remote_name/feature_branch
git push origin remote_name/feature_branch

After the git fetch I recommend to examine situation with gitk --all.
