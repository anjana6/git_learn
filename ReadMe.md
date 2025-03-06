# Git Command

* #### git diff 

    >check changes between working area and staging area

* #### git diff --staged 

    >check changes between staging area and repository area

* #### git diff head 

    > check changes between working area and repository area

* #### git commit -a -m \<commit message> 

    >adding and committing file changes. but can't commit the new file.

* #### git restore --staged \<file name> 

* #### git checkout -b \<branch name> 

     >create new branch

* #### git branch \<branch name> 

    >create new brach but stay in current branch

* #### git branch 

    > see all the branch

* #### git branch -m \<new branch name>

    > rename the branch name

* #### git branch -d \<branch name> 

    >delete the branch (but not delete without merge data to master)

* #### git branch -D \<branch name>

    > delete the branch with all commit and changes

* #### git merge \<branch name> 

    > merge the branch 

        when we create new branch from master branch and do some changes on new branch and commit it and not did any commit in master branch until merge the new branch it's called as fast-forward merge.

        when we create new branch from master branch and do some changes and commit it and did some commit in master branch and merge new branch to master branch we have to add new commit for merging

* #### git rebase \<other branch name> 

    > used as alternative to merging. branch updates one branch with another by applying the commits of one branch on top of the commits of another branch. Rebase doesn't preserve history.

* #### git rebase -i \<other branch name>

    > interactive rebase (combine multiple commit to single commit [s-squase])

* #### git merge --abort 

    > stopping merging

* #### git rebase --abort 

    > stopping rebasing

* #### git commit --amend 

    >update recent commit 

* #### git cherry-pick \<commit hash> 

    > used if you want to apply particular commit from one branch into another branch. mainly used if you don't want to merge the whole branch and you want some of the commits.eg: used for the bug fixes where you want to place that bugfix commit in all the version branches.

* #### git cherry-pick \<commit hash>  \<commit hash>

    > used if you want to apply multiple commit from one branch into another branch.

* #### git reset \<commit hash> --hard 

    > moves the files both working and stating area

* #### git reset \<commit hash> --mixed (default) 

    > moves files only to stage area

* #### git reset \<commit hash> --soft 

    > does not move the files

* #### git reset head --hard 

    > reset last changes 

* #### git stash  

    > stash current changes

* #### git stash list 

    > see all the stashes

* #### git stash pop 

    > take recent stash and remove from stash list
* #### git stash save \<"name"> 

    > stash current changes with name

* #### git stash apply 

    > apply recent stash and not remove from the stash list

* #### git stash apply \<stash id> 

    > apply specific stash 

* #### git stash show -p 

    > see the changes on latest stash

* #### git stash show \<stash id> -p 

    > see the changes on specific stash

* #### git stash drop 

    > recent stash delete

* #### git stash drop \<stash id> 

    > delete specific stash

* #### git stash clear 

    > delete all the stash

* #### git stash branch \<branch name> 

    > create branch with latest stash

* #### git stash branch \<branch name> \<stash id> 

     >create branch with specific stash

* #### git checkout head \<filename> or git checkout --\<filename> 

    > revert the changes of the particular file using. it revert both staging and working area changes

* #### git checkout -  

    > go to the previous one

* #### git restore --stage \<filename> 

    > revert changes from staging area to working area 

* #### git restore \<filename> 

    > revert changes in working area

* #### git switch -c \<branch name> 

    > create new branch

* #### git switch \<branch name> 

    > switch to the branch

* #### git switch -  

    > go to the previous one

* #### git revert \<commit hash> 

    > revert changes and added new commit message

* #### git remote -v 

    > check remote url 

* #### git remote add origin \<url> 

    > add remote url to local repo. if we want, we can change origin as whatever name "gir remote add mygithuburl".

* #### git remote rename \<old-name> \<new-name> 

    > renaming the remotes

* #### git remote remove \<name> 

    > remove the remote

* #### git push \<remote> \<local-branch>:\<remote-branch> 

    > push changes from one branch to another branch

* #### git push -u origin \<branch name> 

    > set upstream 

* #### git branch -r 

    > see remote branch

* #### git fetch \<remote> 

    > this command fetches branches and history from a specific remote repository.it only updates the remote tracking branches.but don't add it into my working directory.

* #### git fetch \<remote> \<branch> 

    > fetch a specific branch from a remote using the command.

* #### git remote add upstream <url>

    >Set the upstream repo

* #### git tag or git tag -l

    > view all the tags

* #### git tag \<name> 

    > can search tag by name

* #### git tag \<name*>

    > can search tag by name. That should be start by that name

* #### git tag \<*name*>

    > can search tag by name, name may be anywhere

* #### git tag \<tagname(V1.0.0)>

    > create tag. This is called as lightweight tag

* #### git tag -a <tagname(V1.0.0)>

    > create tag. This is annotated tag.you can add extra details to tag.

* #### git show <tagname> 

    > can see the tag details.

* #### git push origin <tagname>

    > push specific tag to remote repo

* #### git push origin --tags 

    > push all the tags to remote repo

* #### git tag -d <tagname>

    > delete the tag in local

* #### git push origin -d <tagname>

    > delete tag in origin

* #### git push oriign -d <tagname> <tagname>

    > delete multiple tag in origin

* #### git tag <tagname> <referencecommit>

    > create tag for pass commit 

* #### git reflog show head 

    > can see the behavior of head via the logs. those logs are deleted after 90days.

* #### git reflog show <branch> 

    > can see behavior of branch via the logs. This reflog mainly when we get back deleted commit. because we can see all the action using reflog command.

* #### git reflog show master@{one.day.ago || 1.week.ago}

    > can see one day ago logs

* #### git config --global alias.br "branch"

    > you can set alias and the you can use br instead of branch
    eg: git branch = git br