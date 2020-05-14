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

```gitattributes
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
```
### 3. Use add and commit ###

```gitattributes
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

```gitattributes
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

New branch will be at github repository. Click compare and pull request. Can add comments about changes here.  Then click <Create Pull Request> button. 
  
Then it can be reviewed by click on hyperlink below comments on Pull Requests tab. Then can start a review. Then someone else can approve it (can't approve your own) and merge pull request (ideally someone else does this). 


Make a new branch and add changes: 

```gitattributes
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (master)
$ git branch bigfeature


Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git add .

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git commit -m" reverting back to old title"
[bigfeature fffee0c]  reverting back to old title
 1 file changed, 1 insertion(+), 1 deletion(-)

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git push --set-upstream origin bigfeature
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 328.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'bigfeature' on GitHub by visiting:
remote:      https://github.com/robhami/background-generator/pull/new/bigfeature
remote:
To https://github.com/robhami/background-generator.git
 * [new branch]      bigfeature -> bigfeature
Branch 'bigfeature' set up to track remote branch 'bigfeature' from 'origin'.

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git status
On branch bigfeature
Your branch is up to date with 'origin/bigfeature'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")
```

Make another change: 


### 5. Git merge ###

```gitattributes

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git add .

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git commit -m "added exclamation"
[bigfeature 6f5ff62] added exclamation
 1 file changed, 1 insertion(+), 1 deletion(-)

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/js/bground_gen/background-generator (bigfeature)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 302 bytes | 302.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/robhami/background-generator.git
   fffee0c..6f5ff62  bigfeature -> bigfeature


Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (master)
$ git branch conflict

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (master)
$ git branch conflict
fatal: A branch named 'conflict' already exists.

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (master)
$ git checkout conflict
Switched to branch 'conflict'
```

Now go and remove h1 line completely and save. Then someone else merges big feature on GitHub. Now you add the conflict branch: 

```gitAttributes

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git status
On branch conflict
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git add .

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git commit -m "check"
[conflict b82219d] check
 1 file changed, 1 insertion(+), 1 deletion(-)

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (master)
$ git pull
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 5 (delta 3), reused 2 (delta 2), pack-reused 0
Unpacking objects: 100% (5/5), 1.38 KiB | 2.00 KiB/s, done.
From https://github.com/robhami/background_generator
   b2b8215..74691cf  master     -> origin/master
 * [new branch]      bigfeature -> origin/bigfeature
Updating b2b8215..74691cf
Fast-forward
 index.html | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (master)
$ git checkout conflict
Switched to branch 'conflict'

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git merge master
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.

```

This merge command from GitBash causes conflict as shown above. It also adds text to index.html code

```javascript

<!DOCTYPE html>
<html>
<body id="gradient">

<<<<<<< HEAD
	
=======
	<h1>Background Generator</h1>
>>>>>>> master
	<input class="color1" type="color" name="color1" value="#00ff00">
	<input class="color2" type="color" name="color2" value="#ff0000">

	<h2>This is the background</h2>

	<h3></h3>
	<button class="random" type="text" >Random gradient selector</input>
	

</body>
</html>
<script type="text/javascript" src="script.js"></script>


```

<<<<<<< HEAD
	
======= is where user who added conflict branch is at. It shows that here to the end h1 is missing. but the master does have it. Can just remove the 
<<<<<<< HEAD

Then add, commit and push:
	
=======


```gitAttributes
Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict|MERGING)
$ git status
On branch conflict
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict|MERGING)
$ git add .


Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict|MERGING)
$ git commit -m"fixing merge issue"
[conflict 969ce8a] fixing merge issue

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git status
On branch conflict
nothing to commit, working tree clean

Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git push
fatal: The current branch conflict has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin conflict


Rob@Rob-Laptop MINGW64 ~/Documents/coding/zero_to_mastery/git/background_gen_2/background_generator (conflict)
$ git push --set-upstream origin conflict

Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 610 bytes | 610.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote:
remote: Create a pull request for 'conflict' on GitHub by visiting:
remote:      https://github.com/robhami/background_generator/pull/new/conflict
remote:
To https://github.com/robhami/background_generator.git
 * [new branch]      conflict -> conflict
Branch 'conflict' set up to track remote branch 'conflict' from 'origin'.

```

Go back to GitHub, conflict branch shows but has " No commit comments for this range" because we reverted all the changes. Reviewer can create pull request. Then user can keep working. 

Create a pull request just puts your changes up for review. 











