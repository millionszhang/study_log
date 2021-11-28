21/11/23

### 1.报错 Error: Node Sass does not yet support your current envi



![image-20211123101632020](C:\Users\zyw18\AppData\Roaming\Typora\typora-user-images\image-20211123101632020.png)







vue报错代码如下

Module build failed: Error: Node Sass does not yet support your current environment: Windows 64-bit with Unsupported runtime (93)

解决方案

解决办法其实很简单，就是sass不支持当前的环境，那么在当前环境重新安装一下就好了

先卸载：（***如果卸载不成功，直接找到node-sass文件夹，删除\***）

解决代码如下

cnpm uninstall --save node-sass 

cnpm install --save node-sass 



### 2.Vue项目启动后页面为空白解决方案

![img](https://img-blog.csdnimg.cn/20190422095905461.?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MzI1NDY3Ng==,size_16,color_FFFFFF,t_70)



之前打包的时候有问题，网上有解决方案说更改build中assetsPublicPath的路径，可能自己改错了位置，build和dev中的assetsPublicPath的路径不同，

dev中 assetsPublicPath： /

build中 assetsPublicPath：./

今后多注意‘



#### vue 文件









