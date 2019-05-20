# git指令
```sh
git branch 查看本地分支
git branch -a 查看本地以及远端分支
git branch -v 查看本地分支的head
git branch -vv 查看本地分支以及指向的远端分支的head
git remote -v 查看fetch
git log -p 查看单一文件的更改记录
git checkout + branch name 切换到没有分支
git checkout -b + branch name 创建新的分支并切换到改分支
git push -u + remote branch 提交到远端并追踪该远端
```
# 工作流程
- 在个人电脑安装git 或者是其他git工具
- 执行ssh-keygen -t rsa -C "个人email地址" 生成公钥 发给运维添加权限
- 获取git仓库地址
- 执行git clone + 仓库地址拉取代码
- 执行git branch -a 查看本地以及远端分支
- 执行git checkout -b 本地分支  远端分支 把远端线上分支以及开发分支checkout到本地
- 在开发分支执行git checkout -b 分支名 创建自己的开发分支
- 在个人开发分支开发完毕的代码提交commit
- 切换到项目开发分支，执行git pull 拉取最新代码
- 通过git cherry-pick 指令将个人开发分支提交的commit cherry-pick到项目开发分支
- 提交到项目开发分支远端，测试
- 测试没问题再把项目开发分支的commit cherry-pick到项目线上分支 提交到线上分支
