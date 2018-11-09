git 运用说明

一、配置
1 在项目所在目录，右键点击 Git Bash Here

2 初始化 git 命令：git init

3 自定义设置当前使用 用户
命令：git config --global user.name "transecond"

4 定义邮箱
命令：git config --global user.email "lhaigevv@163.com"

二、如何将代码放入仓库中

1 把代码存储到.git仓库门口  add后是 当前目录下对应的文件路径
命令 git add ./readme.md

2 将代码放入 仓库的房间里 -m 后面是 对文件的简单说明
命令 git commit -m "git运用说明书"

第二个功能 重新添加
git add ./readme.md  可以用tap键自动补齐文件名
// 如果 输入有误会进入到另一个界面
处理方法 按下 esc键 输入引文版:号，输入q 回车
如果退出不了 按下 esc键 输入引文版:号，输入q! 回车  强制退出
git commit -m "git运用说明 更新"

三、继续添加 新功能说明
查看当前状态
git status

四、新添加的功能

五、添加新功能 添加了新文件 后面没有文件路径 会把修改过的文件全部添加进去
git add ./

六、新功能 一次性添加修改过的代码已经目录
git commit --all -m "一次性添加"

七、新功能 忽略文件
在目录文件中新建，.gitignore文件，在文件中添加，需要忽略的文件
/idea.txt
/.gitignore
/css 会忽略掉整个目录文件

八、查看 添加的日志
git log

九、重新添加 第二个功能
git log --oneline 简洁版

十、版本返回  用索引并不准确
git reset hard Head~0  1,2,3

十一、版本返回 版本号通过 git log --oneline
      git reflog 查看历史版本号

git reset hard 版本号

十二、分支存储 用于存储没有写好的代码，利于运行
1、假如现在代码只完成了一半，先创建分支  dev为分支名
git branch dev

查看分支
命令：git branch

切换分支
git checkout dev

假如 代码已经完成
先添加完成的代码
git add ./
git commit -m "添加完成的代码 在dev中提交的"

// 将dev中的代码合并到master中

先切换到 master
git checkout master

// 合并
git merge dev

十三、删除分支 dev为要删除的分支名  删除当前分支必须，切换到当前分支，之外
git branch -d dev

新功能完成了 5

GitHub
不是git 它是一个网站，提供了运行通过git上次代码的功能
在网站中注册
账号：fable
密码 fablesun911**
https://github.com/fablesun/testWeb.git 生成的上传链接地址

上传到网站上的命令  上传的是本地的master分支   push 推
git push https://github.com/fablesun/testWeb.git master

运行 git log 时退不出去 按 q 退退出

下载网站  pull 拉   拿到远程 master分支  比较常用
先在本地初始化一个新的仓储
git pull https://github.com/fablesun/testWeb.git master

另一个办法 clone 克隆 会帮您先创建一个仓库名  第一次使用会用 clone
git clone https://github.com/fablesun/testWeb.git
多次执行 会覆盖本地内容

## 流行框架
## 1 ssh方式上传代码 可以通过不通过用户名密码上传
公钥、私钥  两者之间是有关联的
创建命令：rsa 命令方式
ssh-keygen -t rsa -C "邮箱"
在C盘中，用户，中的文件夹 找到 .ssh文件 用记事本打开公钥复制
在 GitHub 网站中 点击 setting设置 在左侧 ssh中进行配置 生成密匙

创建一个新的文件夹 在新的文件夹中运行 git
我的ssh 地址
git@github.com:fablesun/testWeb1.git
命令
git push git@github.com:fablesun/testWeb1.git master

git@github.com:fablesun/demoWeb.git

创建 全局用户名邮箱
git config --global user.name "用户名"
git config --global user.email "邮箱"

## 本地提交后
先 pull 再 push

## 本地提交后
先 pull 再 push
当有冲突时，会弹出 冲突说明 按 esc 后输入 :wq退出


地址简写方式 git@github.com:fablesun/demoWeb.git

git remote add origin [地址名]

添加时简写
git push origin master

没有修改如何冲突



