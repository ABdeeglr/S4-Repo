# HOW TO USE GIT

初始化：

```bash
git config --global user.name "ABdeeglr"
git config --global user.email "abdeeglr@icloud.com"
```

基本操作：

```bash
git add *file_name*
git commit -m "information"
git status
git log
git diff *file_name*
git checkout -- *file_name* #!丢弃当前暂存区的内容，放弃修改
git rm *file_name* #!从git的版本库中删除某文件
git checkout -- *file_name* #!从git的版本库中恢复某文件
```

版本回退:

````bash
git reset --hard HEAD^
git reset --hard 1904a #!版本号
````

## REMOTE SETTINGS

**生成SSH-KEY**

查看用户主目录下是否存在`.ssh`文件夹，如果有，则在其中查看SSH-key。如果无，遵循一下步骤生产SSH-key

```bash
ssh-keygen -t rsa -C "abdeeglr@icloud.com"
```

在GitHub的User account Setting寻找SSH-key设置，并且按照提示的格式添加公钥。凡是在GitHub的账户中添加的公钥，个人终端可以根据私钥来获得commit的权限，换言之，给每一台电脑注册一对私钥和公钥，然后将公钥注册到GitHub的个人账户中，就能在不同电脑上提交commit.

**远程提交**

将本地库添加到远程库

```bash
git remote add origin git@github.com:ABdeeglr/S4-Repo.git
```

将本地库中的当前分支master与远程库的origin分支相关联并推送

```bash
git push -u origin master
```

关联之后的推送

```bash
git push origin master
```



