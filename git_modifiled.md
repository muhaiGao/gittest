# 撤销修改
## 旧版本：git checkout
### 两种情况：
* 一种是file自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
* 一种是file已经添加到暂存区后，又做了修改，现在，撤销修改就回到添加到暂存区后的状态。
*总之，就是让file回到最近一次git commit 或 git add 时的状态。*

+ 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- <file>.

+ 场景2：当你不但改乱了工作区某个文件内容，还添加到了暂存区时，想丢弃修改，分两步：
1. 使用命令$ git reset HEAD <file>,就回到场景1.
2. 按场景1操作：$ git checkout -- <file> 

+ 场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，使用命令:$ git reset --hard <commit_id>
*用git log 可以查看提交历史，以便确定回退到哪个版本* 
*用git reflog 查看命令历史，以便确定要回到哪个版本*
*可以使用:git reset --hard HEAD^ 或 git reset --hard HEAD~<num>;*




