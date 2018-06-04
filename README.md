# 使用方法



中文 | [English](README_EN.md)

***



### 添加依赖

在根project下的 **build.gradle** 中添加如下依赖，repositories里需要添加上jcenter()。

```java
buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.baoleiwei:levi-debug:0.0.1'
    }
}
```



### 添加插件

在需要使用到的module下的**build.gradle**中添加插件，例如app模块下：

```java
apply plugin: 'com.baoleiwei.levi'
```



### 增加测试闭包

在需要使用到的module下的 **build.gradle **中添加**greeting**闭包，例如app模块下：

```
greeting{
    message  '一个测试信息来自app'
}

android{
    
}

dependencies{
    
}
```



### Gradle运行task

##### 1.第一种方式

打开Terminal.

windows下输入  **gradle -q hello** 回车运行

mac下输入  **./gradle -q hello** 回车运行

这里 **-q**表示quite，去除了一些其他信息。

接着你就可以在命令行输出中找到你在app/build.gradle中的greeting闭包中配置的message消息。

__注意：这种方式需要你配置gradle环境变量，否则命令行会提示找不到该命令__



##### 2.第二种方式

如下图

![步骤1](https://github.com/baolw/MavenTest/blob/master/image/image_1.png)

在Android Studio的右边选择Gradle，找到你在上几个步骤中，调试的模块（我上面用的是app模块）。

在other中，往下翻找到hello这个task，也可以直接键盘输入hello进行搜索。

找到后双击运行即可。

接着找到如下图

![步骤2](https://github.com/baolw/MavenTest/blob/master/image/image_2.png)

在Android Studio的右下角找到**Gradle Console**

即可看到输出中有你配置的测试massage



# 总结

通过这个项目学会了简单gradle plugin的编写，以及通过bintray-release快速的将库上传到jcenter中，这里的步骤学习可以自行百度。