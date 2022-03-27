
### apk构建流程

1、首先是会将java代码文件、aidl等文件，打包成 .class文件；

2、同时资源文件会通过aapt装到一起；

3、.java文件然后会被JAVA编译器转变成.dex文件，接着.dex文件和资源文件会被一起整合成apk；

4、此时的apk只是对源码的封装，因此还需要进行混淆、加固和签名的流程。

#### apk解压后的文件

1）MATE_INFO：主要是版本信息

2）res：主要是放android的资源数据

3）AndroidMainifeast.xml文件，基本跟Android代码中的一样，表示项目的配置清单

4）resources.arsc：主要是包含多语种的这样一些资源信息

5）classes.dex：这个主要就是代码编译后的文件，包含很多方法。如果一个包内方法数超过65535（包内每一个方法都会分配一个short类型的id），那么就需要分包，分包的话就会产生多个class.dex文件。


### gradle作用

1、打包：apk包、插件包

2、hook插件

3、自动化构建

4、自动化签名
