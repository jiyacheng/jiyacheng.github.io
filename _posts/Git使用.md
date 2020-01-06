git操作

### 1.基本知识

![1567514002762](C:\Users\纪亚成\AppData\Roaming\Typora\typora-user-images\1567514002762.png)





![l1567516464377](C:\Users\纪亚成\AppData\Roaming\Typora\typora-user-images\1567516464377.png)

![img](https://github.com/DickyQie/Tool-use/blob/git-learning-document/Git%E5%91%BD%E4%BB%A4.jpg?raw=true)

git checkout . 放弃当前操作

将github端更新至本地仓库: git pull origin 分支 拉取最新

### 2.git上传Github

输入name:$ git config --global uesr.name 'jiyacheng'

输入email:$ git config --global uesr.email '2715869029@qq.com'

初始化：git init

克隆仓库到本地：$ git clone https://github.com/jiyacheng/test1.git

进入仓库：cd test1

更改权限：vi .git/config

>[remote "origin"]
>        url = https://jiyacheng:19980609jyc@github.com/jiyacheng/test1.git

 ==修改==:url = https://name:password@github.com/jiyacheng/test1.git

建立新文件：touch a.cpp ==or== vi a.cpp

上传文件到暂存区: git add a.cpp

> ==若将本地文件全部更新至Github则改为git add *,后面步骤相同==

将文件上传到本地仓库：git commit -m '语句描述'

本地仓库上传导Github: git push

### 3.删除文件

 rm -rf 1.cpp

 git rm 1.cpp

git commit -m 'delete'

git push

### 4.错误

1.将本地的冲突文件冲掉，不仅需要reset到MERGE-HEAD或者HEAD,还需要--hard。没有后面的hard，不会冲掉本地工作区。只会冲掉stage区。

git reset --hard FETCH_HEAD

2.git pull就会成功。

