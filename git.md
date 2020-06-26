## GIT

1. Git和GIThub的区别？

   Git是开发者将源代码存入名位“Git仓库”的资料库并加以使用，而Github则是在网路上提供Git仓库的一项服务

   1. 协作形式的改变
   2. 社会化编程
   3. GIt属于分散性版本管理系统，是为版本管理而设计的软件
   4. 版本管理就是管理更新的历史记录
   5. 集中式：将仓库集中存放在服务器之中，所以值存储一个仓库，集中式将所有数据集中存放在服务器当中，有便于管理的有点。害怕服务器宕机。
   6. 分布式：分布式拥有多个仓库，相对而言稍微复杂。不过，由于本地的开发环境中有仓库，所以开发者不必连接远程的仓库就可以进行开发。fork就是将GIthub的某个特定仓库复制到自己的账户下。

2. 初始化设置

   1. 设置姓名和邮箱地址，请不要使用不方便公开的隐私信息。请不要使用汉字，尽量以英文进行描述。

      ```
      git config  --global user.name
      "Firestname Lastname"
      git config  --global user.email
      "your_email@example.com"
      这个命令会在‘~/.gitconfig'中输出设置文件，更改的话，可以直接编辑这个设置文件。
      ```

   2. 提高命令输出的可读性,各种命令的输出就会变的更容易分辨。

      ```
      git config --global color.ui auto
      ```

   3. 设置头像：在http://cn.gravatar.com 进行上传注册即可

   4. 设置SSH Key：公开密钥. .生成之后会生成id_rsa文件为私有密钥。id_ras.pub为公开密钥。

      ```
      ssh-keygen -t rsa -C
      "your_email@example.com"
      ```

   5. 添加公开密钥：在setting中设置，

      ```
      cat ~/.ssh/id_rsa.pub  可以查看公钥的内容
      ssh -T git@github.com  进行设置
      ```

   6. 社区功能：Follow(关注)，watch(获取最新的开发信息)

   7. 连接仓库，创建仓库，你是会的。必须会markdown语法

3. 基础操作

   1. git init :初始化仓库

      如果初始化成功，生成的.git目录里存储着管理当前目录内容所需要的仓库数据。我们称这个目录是“附属于该仓库的工作树”

   2. git status :查看仓库的状态

   3. git add  xxx : 向缓存区中添加文件 ；缓存区是提交之前的一个临时状态

   4. git commit - m "xxx":保存仓库的历史记录：是将当前缓存区的文件实际保存到仓库的历史记录中。通过这些记录，我们可以在工作树中复原文件；中止提交：请将提交信息留空并直接关闭编辑器，随后提交就会中止

   5. git diff :查看更改前后的差别

      1. 查看当亲工作树海域暂存区的差别：git diff

   6. git log :查看提交日志

      1. 只显示提交信息的第一行：git log --pretty=short
      2. 只显示指定目录或者文件的日志： git  log 文件名或者目录
      3. 显示文件的改动：git log -p //// git log -p 文件名：只查看此文件的修改

      

      

      

      

      

      

      git add <文件名>   将文件加入暂存区

3. git add .   将所有文件加入暂存区
4. git commit -m "<说明>"

#1、创建目录
mkdir project7

#2、进入目录
cd project7

#3、初始化目录为git项目
git init

#4、创建md文件追加内容# project7(一级标题)
echo "# project7" >> README.md

#5、添加说明文件到暂存区
git add README.md

#6、提交到本地仓库并写日志
git commit -m "first commit"

#7、添加远程主机，主机名为origin 地址为https://git.coding.net/zhangguoGit/project7.git
git remote add origin https://git.coding.net/zhangguoGit/project7.git

#8、本地的master分支推送到origin主机，同时指定origin为默认主机，后面就可以不加任何参数使用git push了，-u 参数指定一个默认主机
git push -u origin master





# 下载远程仓库的所有变动
$ git fetch [remote]

# 显示所有远程仓库
$ git remote -v

# 显示某个远程仓库的信息
$ git remote show [remote]

# 增加一个新的远程仓库，并命名
$ git remote add [shortname] [url]

# 取回远程仓库的变化，并与本地分支合并
$ git pull [remote] [branch]

# 上传本地指定分支到远程仓库
$ git push [remote] [branch]

# 强行推送当前分支到远程仓库，即使有冲突
$ git push [remote] --force

# 推送所有分支到远程仓库
$ git push [remote] --all

#简单查看远程---所有仓库
git remote  （只能查看远程仓库的名字）
#查看单个仓库
git  remote show [remote-branch-name]

#新建远程仓库
git remote add [branchname]  [url]

#修改远程仓库
git remote rename [oldname] [newname]

#删除远程仓库
git remote rm [remote-name]

#获取远程仓库数据
git fetch [remote-name] (获取仓库所有更新，但不自动合并当前分支)
git pull (获取仓库所有更新，并自动合并到当前分支)

#上传数据，如git push origin master
git push [remote-name] [branch]



# Bash基本操作命令





https://www.cnblogs.com/best/p/7474442.html#_lab2_3_0

1. cd : 改变目录

   cd ~ 回Home（windows是当前用户所在目录）

   cd . . 回退到上一个目录，直接cd进入默认目录

   pwd : 显示当前所在的目录路径。

   ls(ll): 都是列出当前目录中的所有文件，只不过ll(两个ll)列出的内容更为详细。

   touch : 新建一个文件 如 touch index.js 就会在当前目录下新建一个index.js文件

   rm: 删除一个文件, rm index.js 就会把index.js文件删除

   mv 移动文件, mv index.html src index.html 是我们要移动的文件, src 是目标文件夹,当然, 这样写,必须保证文件和目标文件夹在同一目录下。

   mkdir: 新建一个目录,就是新建一个文件夹

   rm -r : 删除一个文件夹, rm -r src 删除src目录， 好像不能用通配符

   reset 重新初始化终端/清屏

   clear 清屏

   history 查看命令历史。

   help 帮助

   \#表示注释

   echo hello git #git  输出与注释

    echo helloo > 1.txt   往1.txt中写内容 ，会覆盖

   echo 18518020144 >> 1.txt    往1.txt中写内容 ，会追加

    显示文件内容 cat     cat 1.txt     打印1.txt中的内容

2. Git 配置

   使用git config -l 可以查看现在的git环境详细配置

   查看系统config  git config --system --list

   查看当前用户（global）配置  git config --global  --list

   查看当前仓库配置信息 git config --local  --list

3. 设置邮箱名和用户名

    git config --global user.name "zhangguo"  #名称

   git config --global user.email zhangguo@qq.com   #邮箱

   只需要做一次这个设置，如果你传递了--global 选项，因为Git将总是会使用该信息来处理你在系统中所做的一切操作。如果你希望在一个特定的项目中使用不同的名称或e-mail地址，你可以在该项目中运行该命令而不要--global选项。 总之--global为全局配置，不加为某个项目的特定配置。





# Git 常用操作

1. git init                                                 在当前目录新建一个Git代码库，即初始化

   git init [project-name]                         新建一个目录，将其初始化为Git代码库

2. git clone [url]

3.  git add 1.txt                                       把readme.md 添加到git暂存区中

4.  git commit -m "test"                            提交readme.md  -m 后面是说明

5.  git status                                            查看状态

6.  git checkout -b develop                     创建develop分支，并且进入develop分支

7. git status 1.txt                  查看1.txt的状态

   git status   查看所有的文件的状态

8. git add [file1] [file2]    添加指定文件到暂存区

   git add [dir]        添加指定目录到暂存区，包括子目录

   git add   添加当前目录的所有文件到暂存区

9. git rm --cached 3.txt     直接从暂存区删除文件，工作区则不做出改变

10.   git reset HEAD 1.txt     当执行 “git reset HEAD” 命令时，暂存区的目录树会被重写，被 master 分支指向的目录树所替换，但是工作区不受影响。

11.   git clean -df    移除所有未跟踪文件  一般会加上参数-df，-d表示包含目录，-f表示强制清除

12. git rm --cached readme.txt  只从stage中删除，保留物理文件

13. git rm readme.txt   不但从stage中删除，同时删除物理文件

14. git mv a.txt b.txt    把a.txt改名为b.txt

15. 查看文件修改后的差异 git diff [files]  git diff 1.txt

16. 比较暂存区的文件与之前已经提交过的文件   git diff --cached

17. 1比较repo与工作空间中的文件差异   git diff HEAD~n

18. ```
    $ git checkout branch
    #检出branch分支。要完成图中的三个步骤，更新HEAD以指向branch分支，以及用branch  指向的树更新暂存区和工作区。
    
    $ git checkout
    #汇总显示工作区、暂存区与HEAD的差异。
    
    $ git checkout HEAD
    #同上
    
    $ git checkout -- filename
    #用暂存区中filename文件来覆盖工作区中的filename文件。相当于取消自上次执行git add filename以来（如果执行过）的本地修改。
    
    $ git checkout branch -- filename
    #维持HEAD的指向不变。用branch所指向的提交中filename替换暂存区和工作区中相   应的文件。注意会将暂存区和工作区中的filename文件直接覆盖。
    
    $ git checkout -- . 或写作 git checkout .
    #注意git checkout 命令后的参数为一个点（“.”）。这条命令最危险！会取消所有本地的  #修改（相对于暂存区）。相当于用暂存区的所有文件直接覆盖本地文件，不给用户任何确认的机会！
    
    $ git checkout commit_id -- file_name
    #如果不加commit_id，那么git checkout -- file_name 表示恢复文件到本地版本库中最新的状态。
    ```

主目录下建立".gitignore"文件

1. 忽略文件中的空行或以井号（#）开始的行将会被忽略。
2. 可以使用Linux通配符。例如：星号（*）代表任意多个字符，问号（？）代表一个字符，方括号（[abc]）代表可选字符范围，大括号（{string1,string2,...}）代表可选的字符串等。
3. 如果名称的最前面有一个感叹号（!），表示例外规则，将不被忽略。
4. 如果名称的最前面是一个路径分隔符（/），表示要忽略的文件在此目录下，而子目录中的文件不忽略。
5. 如果名称的最后面是一个路径分隔符（/），表示要忽略的是此目录下该名称的子目录，而非文件（默认文件或目录都忽略）。

#为注释
*.txt #忽略所有 .txt结尾的文件
!lib.txt #但lib.txt除外
/temp #仅忽略项目根目录下的TODO文件,不包括其它目录temp
build/ #忽略build/目录下的所有文件
doc/*.txt #会忽略 doc/notes.txt 但不包括 doc/server/arch.txt

# 提交暂存区到仓库区
$ git commit -m [message]

# 提交暂存区的指定文件到仓库区
$ git commit [file1] [file2] ... -m [message]

# 提交工作区自上次commit之后的变化，直接到仓库区，跳过了add,对新文件无效
$ git commit -a

# 提交时显示所有diff信息
$ git commit -v

# 使用一次新的commit，替代上一次提交
# 如果代码没有任何新变化，则用来改写上一次commit的提交信息
$ git commit --amend -m [message]

# 重做上一次commit，并包括指定文件的新变化
$ git commit --amend [file1] [file2] ...





# 列出所有本地分支
$ git branch

# 列出所有远程分支
$ git branch -r

# 列出所有本地分支和远程分支
$ git branch -a

# 新建一个分支，但依然停留在当前分支
$ git branch [branch-name]

# 新建一个分支，并切换到该分支
$ git checkout -b [branch]

# 新建一个分支，指向指定commit
$ git branch [branch] [commit]

# 新建一个分支，与指定的远程分支建立追踪关系
$ git branch --track [branch] [remote-branch]

# 切换到指定分支，并更新工作区
$ git checkout [branch-name]

# 切换到上一个分支
$ git checkout -

# 建立追踪关系，在现有分支与指定的远程分支之间
$ git branch --set-upstream [branch] [remote-branch]

# 合并指定分支到当前分支
$ git merge [branch]

# 选择一个commit，合并进当前分支
$ git cherry-pick [commit]

# 删除分支
$ git branch -d [branch-name]

# 删除远程分支
$ git push origin --delete [branch-name]
$ git branch -dr [remote/branch]

1.

2.$ git config --global user.name "陈"                  绑定名字  自报家门
3.$ git config --global user.email "czfzxzyq@163.com"      绑定邮箱   自报家门
$ git add ./readme.md                                  把readme.md 添加到git中
$ git commit -m "test"                                提交readme.md  -m 后面是说明
esc  ：q!                                              强行退出
$
$ git commit --all -m "这是一次性操作"
$ git add ./                                    把本文件下所有的修改或新建的文件从新上传到缓存区
$git log          记录我们每次提交
$ git log --oneline     日志一行显示
$ git log --pretty=oneline # 格式化输出信息
$ git reset --hard HEAD^ # 当前版本HEAD,上一个版本HEAD^,上上个版本HEAD^^
$git reset --hard Head~0     回退一次，时光逆流,回退放到指定版本；回退到上一次代码提交时候状态；
$git reset --hard 80ed1c1  通过版本号，可以精确回退到指定状态。可以前进和后退。
git reflog         如果关闭了，通过这种方式可以看到所有的版本号；可以看到每一次对版本操作的记录。
$ git branch dev   创建分支dev  git checkout -b login   创建并且跳转到login 分支
$ git branch      查看分支
$ git checkout dev  切换到dev分支
$ git merge dev    dev和master合并；
$ git branch -d sm   删除sm分支；不能自己删除自己；         合并时，有冲突，需要手动处理，然后再提交；
$ git push https://github.com/code1992-clown/abc.git  master   把本地文件添加到github上；
$ git pull https://github.com/code1992-clown/abc.git master    从github上下文件，注意:本地要初始化一个仓储；
$ git clone https://github.com/code1992-clown/abc.git           多次操作会覆盖本地内容，会得到远程仓库的相同数据；
$ git push git@github.com:code1992-clown/testtest.git master   和http 形式的一样
ssh keygen -t rsa -C "czfzxzyq@163.com"             生产公钥和私钥
git push -u master   -u作用是：关联，下次上传时，不用再写master


git remote add origin git@github.com:code1992-clown/vue_shopping.git 连接已经有的仓库
git push -u origin master


# 查看difference
$ git diff



# 丢弃工作区的修改，回到最近一次git commit或git add时的状态：
$ git checkout -- README.md
。。。

# 从版本库中删除该文件
$ git rm README.md


# 测试是否成功
$ ssh -T git@github.com





$ ssh-keygen -t rsa -C "youremail@example.com"
# 测试是否成功
$ ssh -T git@github.com

# 把一个已有的本地仓库与之关联
$ git remote add origin git@github.com:Windrivder/Windrivder.git

# 把本地库的所有内容推送到远程库上（推送master分支的内容）
$ git push -u origin master

# 向远程库推送更新
$ git push origin master

# 从远程库克隆
$ git clone git@github.com:michaelliao/gitskills.git




# 创建+切换dev分支
$ git checkout -b dev

# 相当于
$ git branch dev # 创建分支
$ git checkout dev

# 查看当前分支，当前分支前面标有×号
$ git branch

# 切换回master分支
$ git checkout master
# 查看分支合并情况
$ git log --graph --pretty=oneline --abbrev-commit


# 修改readme.txt文件，并提交一个新的commit
$ git add readme.txt
$ git commit -m "add merge"



# 如果需要临时修复Bug，可以把当前工作现场“储藏”起来，等Bug修复后恢复现场后继续工作
$ git stash