>```
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 681 bytes | 681.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: error: GH007: Your push would publish a private email address.
remote: You can make your email public or disable this protection by visiting:
remote: http://github.com/settings/emails
To github.com:gengwg/xxxxx.git
 ! [remote rejected] master -> master (push declined due to email privacy restrictions)
error: failed to push some refs to 'git@github.com:gengwg/xxxxx.git'


`Solution:`

>
git config --global user.email "526473+gb96@users.noreply.github.com"
git rebase -i
git commit --amend --reset-author
git rebase --continue
git push


>Basic commands

```shell

git init 

git add <directory or file>

git branch -M rename_branch_name # -M rename branch from default(master to branch_name)

git checkout -b new_branch_name # -b create new branch

git commit -m "message"  #-m message

git remote add origin https://github.com/username/repo_name.git

git push -u origin branch_name # -u upstream


PULL

git pull origin branch_name

```
