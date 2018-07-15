# 项目介绍
该项目为父模块
# 子模块应用场景
> 当你在一个项目上工作时，你需要在其中使用另外一个项目。也许它是一个第三方开发的库或者是你独立开发和并在多个父项目中使用的。这个场景下一个常见的问题产生了：你想将两个项目单独处理但是又需要在其中一个中使用另外一个。
# 如何创建子模块
1. 在github创建两个库fatherRep、subRep分别表示父模块、子模块(也可以直接使用其他库)
2. 把父模块clone到本地

        git clone git@github.com:812913/fatherRep.git
3. 进入到父模块所在文件

        cd fatherRep
4. 把子模块添加到父模块中

        git submodule add git@github.com:812913/subRep.git
5. 发现在当前目录下多了一个subPro文件夹和.gitmodules文件
其中.gitmodules文件内容如下：

        [submodule "subRep"]
            path = subRep
            url = git@github.com:812913/subRep.git
    其中path表示子模块的相对路径，url表示子模块的github地址。

    如果你有多个子模块，这个文件里会有多个条目。

    子模块和其它文件一样，处于版本控制之下。