# adding_branches_to_GIT



### 1. git branch command ###

use this to check for branches. Then add a branch.

```gitattributes
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git branch
* master

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git branch littlefeature

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git branch
  littlefeature
* master
```

### 2. git checkout command ###

use this to set directory to a branch
```
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git checkout littlefeature
Switched to branch 'littlefeature'

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (littlefeature)
$ git status
On branch littlefeature
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

```
### 3. Use add and commit ###

```
no changes added to commit (use "git add" and/or "git commit -a")

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (littlefeature)
$ git add .

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (littlefeature)
$ git status
On branch littlefeature
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html


Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (littlefeature)
$ git commit -m "changing text"
[littlefeature 6d614c3] changing text
 1 file changed, 1 insertion(+), 1 deletion(-)
```


### 4. Use push with origin defined ###

Initially, need to define origin to tell to but branch of github repository where you cloned from. 

```
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (littlefeature)
$ git push --set-upstream origin littlefeature
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (14/14), 2.25 KiB | 2.25 MiB/s, done.
Total 14 (delta 4), reused 7 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
remote:
remote: Create a pull request for 'littlefeature' on GitHub by visiting:
remote:      https://github.com/robhami/background-generator/pull/new/littlefeature
remote:
To https://github.com/robhami/background-generator.git
 * [new branch]      littlefeature -> littlefeature
Branch 'littlefeature' set up to track remote branch 'littlefeature' from 'origin'
```

Believe that once origin defined once you dont have to do it again. Next time you can just use "git push". 

New branch will be at github repository. Can open it up and add comments. Then click <Create Pull Request> button. 
  
Then it can be reviewed by click on hyperlink below comments on Pull Requests tab. Then someone else can approve it (can't approve your own) and merge pull request (ideally someone else does this). 



```
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (master)
$ git branch bigfeature

