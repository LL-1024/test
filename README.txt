运行Git Bash
cd e/git		#切换到E盘git目录下
mkdir test		#新建test目录
cd test
#上述两步可合并为 mkdir test && cd test

git init		#初始化，设置test目录为git仓库

touch README.txt	#新建README.txt文件
vi README.txt		#打开README.txt进行编辑
#上述两步可合并为 touch README.txt && vi README.txt

mkdir new
touch new		#无法新建文件，同一目录下，不允许目录与文件名相同
touch new.txt		#添加后缀可以创建
rm new.txt		#删除文件new.txt
rmdir new		#删除目录new
clear			#清屏

mkdir test1
mkdir test1/test1.1	#此时仍在test目录下
touch test1/test1.txt
touch test1/test1.1.txt
echo "Hello test1" >> test1/test1.txt	#在文件末尾，另起一行添加引号内的内容
echo "Hello test1.1" >> test1/test1.1/test1.1.txt
#上述操作可以避免多次切换文件夹操作，但实际项目中，可以结合cd命令操作

ls			#列举当前目录下的内容
ls -a			#列举当前目录下的内容、隐藏内容
ls -al			#列举当前目录下的内容、隐藏内容、详细信息

git add README.txt test1/test1.txt	#将README.txt和test1.txt添加到暂存区
#git add .命令将提交当前目录下所有内容（目录和文件）

git commit -m "提交说明"	#将暂存区内容提交到本地仓库
#tips：提交说明最好以一行短句子作为开头，来简要描述一下这次commit所作的修改(最好不要超过50个字符)；然后空一行再把详细的注释写清楚。这样就可以很方便的用工具把提交说明变成email通知，第一行作为标题，剩下的部分作为email的正文。

git status		#查看提交
