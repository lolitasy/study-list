cd 项目文件夹
git init  //增加索引
git status //查看文件
git add .   //加入档案
git commit -m "注释"
//本地就产生了一个节点

git remote -v //查看链接

//github和git做链接
git remote add origin https://github.com/lolitasy/webrexco.git

origin	https://github.com/lolitasy/webrexco.git (fetch)
origin	https://github.com/lolitasy/webrexco.git (push)

//把文件上传到云端的分支
git push origin master
git pull --rebase origin master

建立新的分支
git checkout -b "b1"

vim b1.text
git add .
git commit -m "新增分支"
git push origin b1

b1传到master
git push origin b1:master