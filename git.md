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

