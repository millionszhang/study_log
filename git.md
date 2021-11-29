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

1.初始化本地仓库

```bash
git init
```

2.将所有文件添加到本地仓库（也可添加你所需的文件）

```bash
git add .
```

3.将项目提交到本地git仓库 （“first commit” 是备注信息）

```bash
git commit -m "first commit"
```


4.本地git仓库与远程仓库关联（两种方式：1.https方式；2.SSL方式）

```bash
git remote add origin https://github.com/JianhaoChung/DGL_GCNER.git
```

或

```bash
git remote add origin  git@github.com:JianhaoChung/DGL_GCNER.git
```

5.将项目推送到远程仓库

```bash
git push -u origin master
```
