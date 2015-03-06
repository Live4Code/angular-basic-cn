## 控制器的写法

有的时候我们写的应用就是各种数据的各种增删改查。Angular中的控制器(```Controller```)就是实现这些逻辑的地方。

我们把控制器的代码放到单独的文件中(```main.js```)，这对于我们整理逻辑有很大的好处。

Angular中控制器有自己的作用域(```$scope```)。作用域用HTML元素
来划分，在```index.html```16行加入关键词```ng-controller```,Angular就知道有个控制器来托管这个元素。范围就是到这个元素的结束标签（21行），是不是很容易理解。

在这块区域中，双向绑定```{{ }}```的变量就到对应的```MainCtrl```中查询。这些变量就是Javascript中的变量，但是定义在```$scope```上。$scope是控制器和页面沟通的桥梁，挂在$scope上的变量就自动实现了双向绑定。


## 习题说明
 
**1.** 执行并预览，了解```data.greeting```是怎样传递到页面上的。

**2.** 在```index.html```我们希望第16行上显示 ```Welcome to the Superheroic Javascript MVW Framework```。请在```main.js```中修改及输入与页面相对应的变量来实现。