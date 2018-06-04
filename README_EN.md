# USER GUIDE

[中文](README.md) | English

------



### Add Dependencies

Find **build.gradle** in root project，add info like below code：

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



### Add plugin

Find **build.gradle** in what module that you want to test，add info like below code：

```java
apply plugin: 'com.baoleiwei.levi'
```



### Add test closure

Find **build.gradle** in what module that you want to test，and add **greeting** closure like below：

```
greeting{
    message  '一个测试信息来自app'
}

android{
    
}

dependencies{
    
}
```



### Run gradle task

##### 1.First way

Open Terminal.

In windows , input **gradle -q hello**, then run

In mac, input **./gradle -q hello** , then run

 **-q**represent quite，remove som other unnecessary info.

Then you can find the info in your command line

__Note : This method requires you to configure the gradle environment variable, otherwise the command line will prompt not find the command__



##### 2.Second way

like below：

![步骤1](https://github.com/baolw/MavenTest/blob/master/image/image_1.png)

Find __Gradle__ in Android Studio，Find the module you test in the last few steps (I used the app module above).

Find the __hello__ task in __other__ , or input hello to find.

Then double click to run

Then find like below：

![步骤2](https://github.com/baolw/MavenTest/blob/master/image/image_2.png)

Find **Gradle Console** in Android Studio.

Finally you will find the message you test.



# Summary

Through this project, I learned how to write a simple gradle plugin and upload binaries to jcenter quickly via bintray-release. how to upload binaries you can __Google__.

