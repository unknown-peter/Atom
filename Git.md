

# Git

## Git关联GitHub
1. 在git bash中创建ssh key
    ```bash
    ssh-keygen -t rsa -C "xxx@xxx.com"
    ```
2. 复制id_rsa.pub中的key，在github页面中SSH and GPG keys添加New SSH key
3. 验证
    ```bash
    ssh -T git@github.com
    ```
4. 设置username和email
    ```bash
    git config --global user.name "xxx"
    git config --global user.email "xxx@xxx.com"
    ```


# TortoiseGit

## TortoiseGit关联GitHub
1. 使用PuTTygen生成公钥和私钥，保存私钥文件。
2. 粘贴公钥到github页面中SSH and GPG keys
3. TortoiseGit 设置-Git-远端页面中Putty密钥选择私钥文件
