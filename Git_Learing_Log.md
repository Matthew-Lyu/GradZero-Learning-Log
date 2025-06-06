# Git Learning Log

之前学习过一些git的操作，现在除了基本的提交等操作已经忘记的差不多了，创建这个文档开始记录一些更加完整且规范的git操作。

## SSH

生成ssh密钥

```bash
ssh -keygen -t rsa -b 4096 -C "name"
```

## Git

1. 克隆仓库

   ```bash
   git clone 
   ```

   注意的是，如果克隆很大的仓库，那么需要用--depth来限定克隆的提交数

   ```bash
   git clone ****** --depth 10
   ```

2. 创建新分支并切换

   ```bash
   git checkout -b branch_name
   ```

   或者直接在vscode左下角可以创建分支

3. 合并分支

   ```bash
   git checkout main/master
   git merge other_branch_name
   ```

   报错的话跟随提示继续操作

4. 删除分支

   删除本地分支

   ```bash
   git branch -d branch_name      # 删除已合并的本地分支
   git branch -D branch_name      # 强制删除，即使未合并
   ```

   删除远程分支

   ```bash
   git push origin --delete branch_name
   ```

5. 推送本地分支到远程

   ```
   git push origin branch_name
   ```

   