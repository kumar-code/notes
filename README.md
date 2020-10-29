# Notes

## Git Commands
Git push rejected “non-fast-forward”

It looks, that someone pushed new commits between your last git fetch and git push. In this case you need to repeat your steps and rebase feature_branch one more time.

1. git fetch
2. git rebase remote_name/feature_branch
3. git push origin remote_name/feature_branch

After the git fetch I recommend to examine situation with gitk --all.


## Create a new branch with changes tested on dummy branch

git digest large small newborn "message"

Take the diff changes by comparing large branch (having max commits with recent changes) and small branch (commnly the master branch - to which changes need to be add by creating a copy branch of master with newborn name) and commit the changes with "message" in newborn branch

git config alias.digest '! digest() { git checkout $2 && git checkout -b $3 && git branch tmp $1 && git checkout tmp && git reset --soft $3 && git checkout $3 && git branch -D tmp && git commit -m "$4" && git push origin $3; } ; digest'

git digest dev master bug-fix "Bug fix - 1834"

