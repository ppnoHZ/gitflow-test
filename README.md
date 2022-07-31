# 开始

* 安装
> 参考: [github](https://github.com/nvie/gitflow)

# [命令](https://github.com/nvie/gitflow/wiki/Command-Line-Arguments)

* 初始化：git flow init

    -d 使用默认的分支名字

    -f 强制   

    Initialize a new git repo with support for the branching model.
> git目录执行：git flow init

    >然后询问各个分支的名字，使用默认值即可

    >No branches exist yet. Base branches must be created now.

    >Branch name for production releases: [master]

    >Branch name for "next release" development: [develop]

    >How to name your supporting branch prefixes?

    >Feature branches? [feature/]

    >Release branches? [release/]

    >Hotfix branches? [hotfix/]

    >Support branches? [support/]

    >Version tag prefix? []

* 开始一个新的功能
    > git flow feature start [feature_name]

    会创建一个名字为 feature/feature_name的分支，并切换到feature/feature_name分支



* 完成一个功能的开发
    >git flow feature finish feature_name

    该命令将会把feature/feature_name合并到develope分支，然后删除功能(feature)分支。

* 查看当前所有的功能分支
    -v： 表示输出详情
    > git flow feature 等同 git flow feature list
        * a_feature

    >git flow feature list -v 
        * a_feature   (no commits yet)

* 将一个feature分支推送到远程服务器

    > git flow feature publish feature_name

    或者
    >git push origion feature/featuer_name


* 发布版本
    > git flow release start v0.1.0

    当你在完成（finish)一个发布分支时，它会把你所作的修改合并到master分支，同时合并回develop分支，所以，你不需要担心你的master分支比develop分支更加超前。

* Hotfix

## fetch

## filter

> 更新了密码

# 参考
[使用Git Flow管理开发流程](http://stormzhang.com/git/2014/01/29/git-flow/)
