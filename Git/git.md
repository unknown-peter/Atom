

# Git

## Git关联GitHub
* 在git bash中创建ssh key `$ ssh-keygen -t rsa -C "xxx@xxx.com"`
* 复制id_rsa.pub中的key，在github页面中SSH and GPG keys添加New SSH key
* 输入 `$ ssh -T git@github.com` 验证
* 设置username和email(`git config --global user.name "xxx"` `git config --global user.email "xxx@xxx.com"`)


# TortoiseGit

## TortoiseGit关联GitHub
* 使用PuTTygen生成公钥和私钥，保存私钥文件。
* 粘贴公钥到github页面中SSH and GPG keys
* TortoiseGit 设置-Git-远端页面中Putty密钥选择私钥文件
