# 配置Gradle

Kotlin插件包括一个让我们配置Gradle的工具。但是我还是倾向于保持我对Gradle文件读写的控制权，否则它只会变得混乱而不会变得简单。不管怎么样，在使用自动工具之前知道它是怎么工作的是个不错的主意。所以这次，我们将手动去做。

首先，你需要如下修改父`build.gradle`：
```groovy
buildscript {
    ext.support_version = '23.0.1'
    ext.kotlin_version = '0.13.1514'
    ext.anko_version = '0.7'
    repositories {
jcenter()
    dependencies {
        classpath 'com.android.tools.build:gradle:1.2.3'
        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
} }
allprojects {
    repositories {
jcenter() }
}
```