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




