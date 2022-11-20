# 安装

## Mac

Mac自带git，也可以通过brew安装git。

```bash
$ brew install git

$ git --version
git version 2.24.3 (Apple Git-128)
```

## 简单配置

配置用户信息

```bash
$ git config --global user.name 'laoxu'
$ git config --global user.email 'laoxu@163.com'
```

配置ssh，用于github等线上仓库配置秘钥。

```bash
$ ssh-keygen -t rsa -C "laoxu@163.com" 

# 然后一直回车即可，会生成./ssh文件夹，有rsa和rsa.pub两个文件
```

配置github

- 复制rsa.pub的文件内容
- 进入github，Settings->SSH and GPG keys->New SSH key

## 基本概念

![image-20221120160421685](https://document-1257478771.cos.ap-guangzhou.myqcloud.com/md/202211201604754.png)

## 基本操作

```bash
$ git init # 初始化git项目，多了一个.git文件夹
$ git status # 查看当前状态
$ git add . # 添加所有文件到暂存区
$ git commmit -m 'update' # 提交代码到本地仓库
$ git log # 查看版本，an
$ git branch xx # 创建xx新分支
$ git branch -D xx # 强制删除xx分支，-d软删除
$ git check xx # 切换到xx分支
$ git check -b xx ## 创建并切换到xx分支
$ git merge xx # 将xx分支合并进来
$ git push # 
$ git clone url # 将远程仓库克隆到本地
$ git fetch 
```

## gitignore

生命哪些文件不会被提交到远程仓库, 使用`touch .gitignore`创建文件。

```bash
xxx.jpg # 表示某个文件
./xx/yy # 表示某个文件夹下的所有文件
```

