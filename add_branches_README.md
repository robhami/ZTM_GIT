# ZTM_GIT




```git attributes
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git branch
* master

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git branch littlefeature

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background-generator (master)
$ git branch
  littlefeature
* master

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
