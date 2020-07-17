### git 基础操作

> 
* 从远程拷贝项目 ：git clone url
* 把本地文件添加到仓库 ：git add -A 
  * 查看变化的文件 ：git status
* 提交到本地仓库 ：git commit -m ''
* push到远程(此时可能需要填写git上的账号和密码)：git push 

> 打版本号

* git tag: 查看所有版本号
* git tag -a v1.0.1 -m "说明": 打了v1.0.1的版本号
* git push origin v1.0.1：push到远程
* git show v1.0.1 :输出v1.0.1的详情；按q退出详情查看
* 