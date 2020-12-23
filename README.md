# plugin_demo

A new Flutter plugin.



## Getting Started

本项目为个人学习如何实现，发布，使用一个 Flutter plugin 的例子.  

1.创建一个flutter 工程，
    
    选择 Flutter Plugin,Android studio 自动创建
    
    或者使用命令行创建
    flutter create --org com.liaoli --template=plugin plugin_demo
    其中 com.liaoli 是插件包名的一部分，plugin_name 是插件的名称。插件的完整包名为 com.liaoli.plugin_demo
      
  
2.实现插件代码


3.发布代码
    
    这里是上传到 pub.dev 上面
    
    在上传之前使用如下命令检查插件中的一些问题：
    
    flutter packages pub publish --dry-run
    
    还需要做的就是上传前的需要清理插件，避免插件过大无法上传
    
    flutter clean
    
    使用如下命令进行插件的上传
    
    
    flutter packages pub publish


4.使用插件

   

    pub 依赖
    这种是最常见的方式，直接在 工程的 pubspec.yaml 中依赖
    
    dependencies:
      flutter:
        sdk: flutter
      # 添加 toast 的依赖
      plugin_demo: ^0.1.5
    
    git 依赖
    很多时候，pub 上的某个插件并不能完全满足我们实际的业务需求，如 UI 或者一些逻辑问题，这个时候我们可以将其源码下载下来，
    然后根据自己的业务需求对其进行修改。改完之后通常会上传到公司的私有仓库中（GitHub 或者 GitLab），然后在工程中就需要依赖私有仓库中的库
    
    dependencies:
     plugin_demo:
        git:
          url: http://xxx/plugin_demo.git
    
    还可能依赖该仓库指定分支上的代码，如依赖远程 dev 分支上的代码
    
    dependencies:
      plugin_demo:
         git:
          ref: dev
          url: http://xxx/plugin_demo.git
    
    本地依赖
    有时候需要在项目中测试本地的某个插件，这个时候就可以使用本地依赖的方式来依赖插件
    
    dependencies:
        plugin_demo:
            path: user/xxx/plugin_demo/










