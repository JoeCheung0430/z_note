# GIT的一些用法和指令

## 1、初始化本地git仓库

### 1.1 首次使用全局配置

```shell
git config --global user.name "用户名"
git config --global user.email "邮箱地址"
```

### 1.2 Git仓库初始化

```shell
git init
#查看当前的状态
git status
```

### 1.3 添加到缓存区

```shell
git add 文件名
git add 文件名1 文件名2 文件名3 …
git add .（添加当前目录到缓存区中）
```

1.4 提交到版本库

```shell
git commit -m “注释内容”
```





## 2、将GitHub文件克隆到本地

### 2.1 SSH配置

```shell
#生成密钥文件
cd .ssh
ssh-kengen -t rsa -b 4096
vi *.pub

#GitHub里去设置SSH keys

#在.ssh目录下去创建config文件
# github
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/test
```

### 2.2 将本地仓库push到远程仓库

```
git push
```



## 3、将本地仓库添加到GitHub

### 3.1 添加一个远程仓库

```shell
git remote add origin git@github.com:JoeCheung0430/My_Notes.git
#查看当前仓库所对应的远程仓库的别名和地址
git remote -v
```

### 3.2 指定分支的名称

```shell
git branch -M main
```

### 3.3 把本地的分支和远程的分支关联起来

```shell
git push -u origin main
```

### 3.4 远程仓库pull到本地仓库

```shell
git pull
```



## 4、将本地仓库添加到Gitee

### 4.1Git全局设置

```
git config --global user.name "Joe"
git config --global user.email "10145627+joeeeeeee@user.noreply.gitee.com"
```

### 4.2 SSH配置

```shell
#生成密钥文件
cd .ssh
ssh-kengen -t rsa -b 4096
vi *.pub
```

### 4.3 添加远程仓库

```shell
git remote add origin git@gitee.com:joeeeeeee/my-notes.git
```

### 4.4 查看远程仓库

```shell
git remote
```

### 4.5 推送到远程仓库

```
git push -u origin "master"
```

