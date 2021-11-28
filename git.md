2021/11/22 

git 报错

在clone时get报错

![image-20211122162319602](C:\Users\zyw18\AppData\Roaming\Typora\typora-user-images\image-20211122162319602.png)

解决方案

![image-20211122162336936](C:\Users\zyw18\AppData\Roaming\Typora\typora-user-images\image-20211122162336936.png)

$ git config --global core.longpaths true

$ git clone [git库]

![image-20211122211605729](C:\Users\zyw18\AppData\Roaming\Typora\typora-user-images\image-20211122211605729.png)



```git
//这是我们要clone的
git clone https://github.com/Hackergeek/architecture-samples
 
//使用镜像
git clone https://github.com.cnpmjs.org/Hackergeek/architecture-samples
 
//或者
 
//使用镜像
git clone https://git.sdut.me/Hackergeek/architecture-samples
```

git pull origin master  本地同步远程仓库，将远程仓库里的内容拉下来

git rm -r --cached 文件名   删除文件

git commit -m “delete dir”  提交并添加说明

git push origin master 将本次更改更新到github项目上去
