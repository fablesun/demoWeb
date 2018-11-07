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

<<<<<<< HEAD
=======
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