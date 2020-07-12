1. #### Git和SVN的区别在哪里？

   ```js
   git 和 svn 最大的区别在于 git 是分布式的，而 svn 是集中式的。因此我们不能再离线的情况下使用 svn。如果服务器
   出现问题，我们就没有办法使用 svn 来提交我们的代码。
   svn 中的分支是整个版本库的复制的一份完整目录，而 git 的分支是指针指向某次提交，因此 git 的分支创建更加开销更小
   并且分支上的变化不会影响到其他人。svn 的分支变化会影响到所有的人。
   
   ```

2. #### 常用的git命令有哪些？

   ```js
   git init					// 新建 git 代码库，同时默认创建一个master分支
   git add                      // 添加指定文件到暂存区
   git rm                       // 删除工作区文件，并且将这次删除放入暂存区
   git mv					    //移动或重命名一个文件、目录、软连接
   git commit -m [message]      // 提交暂存区到仓库区
   git branch                   // 列出所有分支
   git checkout -b [branch]     // 新建一个分支，并切换到该分支
   git status                   // 显示有变更的文件
   git clone [url]				//拷贝一个 Git 仓库到本地
   git diff					//查看执行 git status 的结果的详细信息-未还存档改动
   git diff --cached			//查看已缓存的改动
   git diff HEAD				//查看已缓存的与未缓存的所有改动
   git diff --state			//显示摘要而非整个 diff
   git reset HEAD				//用于取消已缓存的内容
   git log						//查看git提交历史
   ```

   

3. #### git pull 和 git fetch 的区别？

   ```js
   git fetch 只是将远程仓库的变化下载下来，并没有和本地分支合并。
   
   git pull 会将远程仓库的变化下载下来，并和当前分支合并。
   ```

   

4. ####  git rebase 和 git merge 的区别？

   ```js
   git merge 和 git rebase 都是用于分支合并，关键在 commit 记录的处理上不同。
   
   git merge 会新建一个新的 commit 对象，然后两个分支以前的 commit 记录都指向这个新 commit 记录。这种方法会
   保留之前每个分支的 commit 历史。
   
   git rebase 会先找到两个分支的第一个共同的 commit 祖先记录，然后将提取当前分支这之后的所有 commit 记录，然后
   将这个 commit 记录添加到目标分支的最新提交后面。经过这个合并后，两个分支合并后的 commit 记录就变为了线性的记
   录了。
   ```
   
   
   
5. 分支管理

   ```js
   创建分支:git branch (branchname)
   切换分支:git checkout (branchname)
   删除分支:git branch -d (branchname)
   
   列出分支:git branch		//没有参数时，git branch 会列出你在本地的分支。
   合并分支:git merge
   ```

   



