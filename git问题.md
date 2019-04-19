``` git
 git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	deleted:    src/main/java/com/youlaiyouqu/uqukid/service/test

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   .idea/workspace.xml

cuihaodeMacBook-Pro:uqukid cuihao$ git add .
cuihaodeMacBook-Pro:uqukid cuihao$ git status
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   .idea/workspace.xml
	deleted:    src/main/java/com/youlaiyouqu/uqukid/service/test

cuihaodeMacBook-Pro:uqukid cuihao$ git commit -m'test'
[dev 8a5f820] test
 2 files changed, 46 insertions(+), 19 deletions(-)
 delete mode 100644 src/main/java/com/youlaiyouqu/uqukid/service/test
cuihaodeMacBook-Pro:uqukid cuihao$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

cuihaodeMacBook-Pro:uqukid cuihao$ git push --set-upstream origin dev
To gitlab.com:youlaiyouqu/uqukid.git
 ! [rejected]        dev -> dev (non-fast-forward)
error: failed to push some refs to 'git@gitlab.com:youlaiyouqu/uqukid.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
cuihaodeMacBook-Pro:uqukid cuihao$ git branch master
fatal: A branch named 'master' already exists.
cuihaodeMacBook-Pro:uqukid cuihao$ git branch
* dev
  master
cuihaodeMacBook-Pro:uqukid cuihao$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
cuihaodeMacBook-Pro:uqukid cuihao$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
cuihaodeMacBook-Pro:uqukid cuihao$ git push
Everything up-to-date
cuihaodeMacBook-Pro:uqukid cuihao$ git checkout dev
Switched to branch 'dev'
cuihaodeMacBook-Pro:uqukid cuihao$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> dev

cuihaodeMacBook-Pro:uqukid cuihao$  git branch --set-upstream-to=origin/dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
cuihaodeMacBook-Pro:uqukid cuihao$ git pull
Auto-merging .idea/workspace.xml
CONFLICT (content): Merge conflict in .idea/workspace.xml
Automatic merge failed; fix conflicts and then commit the result.
cuihaodeMacBook-Pro:uqukid cuihao$ 
cuihaodeMacBook-Pro:uqukid cuihao$ git status
On branch dev
Your branch and 'origin/dev' have diverged,
and have 3 and 2 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Changes to be committed:

	modified:   .idea/misc.xml
	new file:   src/main/java/com/youlaiyouqu/uqukid/dao/test
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ActivityCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ActivityDiscountCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ActivityPinTuanCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ActiviyRegisterCouponCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/CommentCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/CommentImageCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/CouponCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/CouponEntityCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/OrderCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/OrderItemCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/OrderLogCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ProductAttributeNameCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ProductAttributeValueCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ProductCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ProductImageCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ProductSaleAttributeNameCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/ProductSkuCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/UserAddressCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/UserCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/productSaleAttributeValueCustom.java
	new file:   src/main/java/com/youlaiyouqu/uqukid/entity/test
	modified:   src/main/resources/application.yaml

Unmerged paths:
  (use "git add <file>..." to mark resolution)

	both modified:   .idea/workspace.xml

cuihaodeMacBook-Pro:uqukid cuihao$ git add .idea/workspace.xml
cuihaodeMacBook-Pro:uqukid cuihao$ git commit -m'conflict fixed'
[dev 5bba267] conflict fixed
cuihaodeMacBook-Pro:uqukid cuihao$ git push
Enumerating objects: 58, done.
Counting objects: 100% (57/57), done.
Delta compression using up to 8 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (34/34), 4.69 KiB | 1.56 MiB/s, done.
Total 34 (delta 15), reused 0 (delta 0)
remote: 
remote: To create a merge request for dev, visit:
remote:   https://gitlab.com/youlaiyouqu/uqukid/merge_requests/new?merge_request%5Bsource_branch%5D=dev
remote: 
To gitlab.com:youlaiyouqu/uqukid.git
   6ca759b..5bba267  dev -> dev
cuihaodeMacBook-Pro:uqukid cuihao$ 
```
###git push 出现的问题
