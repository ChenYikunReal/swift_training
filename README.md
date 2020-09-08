# Swift入门练习记录

## Swift
![在这里插入图片描述](https://github.com/ChenYikunReal/swift_training/blob/master/images/swift-background.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mzg5NjMxOA==,size_16,color_FFFFFF,t_70)

## Windows使用Swift
![在这里插入图片描述](https://github.com/ChenYikunReal/swift_training/blob/master/images/swift-windows.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mzg5NjMxOA==,size_16,color_FFFFFF,t_70) <br/>

Swift for Windows
- [官方下载地址](https://swiftforwindows.github.io/)
- [备选CSDN下载](https://download.csdn.net/download/m0_47235762/12346913)
- [安装教程](https://blog.csdn.net/weixin_47580695/article/details/105941024)

CLion支持的Swift插件
- [下载地址](https://plugins.jetbrains.com/plugin/8240-swift)

Swift学习
- [Swift官方手册](https://docs.swift.org/swift-book/GuidedTour/GuidedTour.html)
- [Swift中文手册](https://www.runoob.com/manual/gitbook/swift5/source/_book/index.html)
- [Swift源码下载](https://swift.org/download/#latest-development-snapshots)


最终决定放弃CLion，因为CLion认为Windows系统不支持Swift所以也不支持Swift for Windows，所以选VS Code。<br/>

![在这里插入图片描述](https://github.com/ChenYikunReal/swift_training/blob/master/images/vscode.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mzg5NjMxOA==,size_16,color_FFFFFF,t_70)



![在这里插入图片描述](https://github.com/ChenYikunReal/swift_training/blob/master/images/swift-vscode.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80Mzg5NjMxOA==,size_16,color_FFFFFF,t_70)

## 代码的处理方式
MacOS不是很熟悉；Windows使用文本编辑器可编辑，需要使用`Swift for Windows`进行编译。

## Swift关键词
- 与声明有关的关键词
    - class
    - deinit
    - enum
    - extension
    - func
    - import
    - init
    - internal
    - let
    - operator
    - private
    - protocol
    - public
    - static
    - struct
    - subscript
    - typealias
    - var
- 与语句有关的关键词
    - break
    - case 
    - continue
    - default
    - do
    - else
    - fallthrough
    - for
    - if
    - in
    - return
    - switch
    - where
    - while
- 与表达式和类型有关的关键词
    - as
    - dynamicType
    - false
    - is
    - nil
    - self
    - Self 	super
    - true
    - \_COLUMN\_
    - \_FILE\_
    - \_FUNCTION\_
    - \_LINE\_ 	
- 在特定上下文中使用的关键词
    - associativity
    - convenience
    - dynamic
    - didSet
    - final
    - get
    - infix
    - inout
    - lazy
    - left
    - mutating
    - none
    - nonmutating
    - optional
    - override
    - postfix
    - precedence
    - prefix
    - Protocol
    - required
    - right
    - set
    - Type
    - unowned
    - weak
    - willSet

## Swift转义字符
- \0 &emsp;&emsp;:&emsp;空字符
- \\\ &emsp;&emsp;:&emsp;反斜线 \
- \b &emsp;&emsp;:&emsp;退格(BS) ，将当前位置移到前一列
- \f &emsp;&emsp;:&emsp;换页(FF)，将当前位置移到下页开头
- \n &emsp;&emsp;:&emsp;换行符
- \r &emsp;&emsp;:&emsp;回车符
- \t &emsp;&emsp;:&emsp;水平制表符
- \v &emsp;&emsp;:&emsp;垂直制表符
- \\' &emsp;&emsp;:&emsp;单引号
- \\" &emsp;&emsp;:&emsp;双引号
- \000 &emsp;:&emsp;1到3位八进制数所代表的任意字符
- \xhh... &nbsp;:&emsp;1到2位十六进制所代表的任意字符

## Swift运算符
- Swift3 取消了++和--
- 基本运算符：+ - * / %
- 等于确实是==但没有===
- 没有&和|，与或非是&&、||、!
- 左移右移只有\<\<和\>\>
- 区间运算符：`...` 例：`for i in 1...5` 这个是闭区间 而左闭右开区间是：`for i in 1..<5`

## Swift条件语句
- if条件语句不打小括号，直接写逻辑表达式
- switch条件语句不打小括号，直接写逻辑表达式
- switch语句默认break，想继续执行下去可以加一行`fallthrough`
- switch语句的case可以包含多个情况，如`case 1,2`
- 三目运算符也支持，且比较正常：`Exp1 ? Exp2 : Exp3;`

## Swift循环语句
- for循环在Swift3中被弃用，这东西也不打小括号
- for...in还是可以用的
- do...while改成了`repeat...while`，while和repeat...while都不打小括号

## Swift字符串
- String不是Java那种表面可变实则不可变的引用类型，而是由var和let决定是否可变的。
- String支持+=
- 判空用`str.isEmpty`
- 单字符的字符串如`"A"`可以代表Character

## Swift枚举
跟C和Objective-C不同，Swift的枚举成员在被创建时不会被赋予一个默认的整型值。<br/>
不过，只要确定一个枚举值，其余可以自动推导，默认从0开始递增1。

## Swift结构体
Swift 结构体是构建代码所用的一种通用且灵活的构造体。

我们可以使用结构体来定义你的自定义数据类型。<br/>
我们可以为结构体定义属性（常量、变量）和添加方法，从而扩展结构体的功能。

Swift结构体与C和Objective-C不同的是：
- 结构体不需要包含实现文件和接口。
- 结构体允许我们创建一个单一文件，且系统会自动生成面向其它代码的外部接口


对于结构体，需要注意以下内容：

结构体实例总是通过值传递来定义你的自定义数据类型。

按照通用的准则，当符合一条或多条以下条件时，请考虑构建结构体：
- 结构体的主要目的是用来封装少量相关简单数据值。
- 有理由预计一个结构体实例在赋值或传递时，封装的数据将会被拷贝而不是被引用。
- 任何在结构体中储存的值类型属性，也将会被拷贝，而不是被引用。
- 结构体不需要去继承另一个已存在类型的属性或者行为。

举例来说，以下情境中适合使用结构体：
- 几何形状的大小，封装一个width属性和height属性，两者均为Double类型。
- 一定范围内的路径，封装一个start属性和length属性，两者均为Int类型。
- 三维坐标系内一点，封装x，y和z属性，三者均为Double类型。

再次强调：结构体实例是通过值传递而不是通过引用传递。

## Swift类
Swift 类是构建代码所用的一种通用且灵活的构造体，我们可以为类定义属性（常量、变量）和方法。

与其他编程语言所不同的是，Swift 并不要求我们为自定义类去创建独立的接口和实现文件。我们所要做的是在一个单一文件中定义一个类，系统会自动生成面向其它代码的外部接口。

### 类和结构体的对比
Swift 中类和结构体有很多共同点。共同处在于：
- 定义属性用于存储值
- 定义方法用于提供功能
- 定义附属脚本用于访问值
- 定义构造器用于生成初始化值
- 通过扩展以增加默认实现的功能
- 符合协议以对某类提供标准功能

与结构体相比，类还有如下的附加功能：
- 继承允许一个类继承另一个类的特征
- 类型转换允许在运行时检查和解释一个类实例的类型
- 解构器允许一个类实例释放任何其所被分配的资源
- 引用计数允许对一个类的多次引用

## Swift可选元组类型的说明
(Int, Int)?与(Int?, Int?)是不同的。

前者表示表示这个元组是可选的，后者表示对应的元组内元素值是可选的。

## Swift访问权限
|访问级别 | 定义 |
|:---:|:---:|
|public | 可以访问自己模块中源文件里的任何实体，别人也可以通过引入该模块来访问源文件里的所有实体 |
|internal | 可以访问自己模块中源文件里的任何实体，但是别人不能访问该模块中源文件里的实体 |
|fileprivate | 文件内私有，只能在当前源文件中使用 |
|private | 只能在类中访问，离开了这个类或者结构体的作用域外面就无法访问 |



说明：
- Swift模块指的是以独立单元构建和发布的Framework或Application，要通过`import`来调用
- 源文件是单个源码文件，它通常属于一个模块，源文件可以包含多个类和函数的定义
- 子类的访问级别不得高于父类的访问级别
- 常量、变量、属性不能拥有比它们的类型更高的访问级别
- 下标也不能拥有比索引类型或返回类型更高的访问级别
- Setter的访问级别可以低于对应的Getter的访问级别，这样就可以控制变量、属性或下标索引的读写权限
- 我们可以给自定义的初始化方法申明访问级别，但是要不高于它所属类的访问级别。但必要构造器例外，它的访问级别必须和所属类的访问级别相同
- 如同函数或方法参数，初始化方法参数的访问级别也不能低于初始化方法的访问级别
- 欲对协议设置访问权限，必须确保该协议只在申明的访问级别作用域中使用
- 扩展成员应该具有和原始类成员一致的访问级别
- 定义的类型别名都会被当作不同的类型，以便于进行访问控制，但它的访问级别不可高于原类型的访问级别
