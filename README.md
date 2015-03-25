指令一般不会单独存在，通常是依附在控制器中。比如我们的翻页控件，单独的一个翻页控件是毫无意义的，我们需要一个父控制器来掌管对显示内容的翻页。
而具体要显示哪一页的内容则是通过翻页控件来控制。对于这个流程指令和控制器间的数据的共享和传递至关重要。

指令会创建一个独立的“Isolate”作用域，它不会直接访问/修改父作用域的属性，即不会意外的改变了指令所在的控制器中$scope上的变量。
在这种情况下directive与controller进行数据通信有如下方式，

1. ```=``` 指令属性与父作用域的属性进行双向绑定，任何一方的修改均影响到对方

2. ```@``` 指令作用域的属性与父作用域的属性进行单向绑定，指令只能读取

3. ```&``` 指令作用域与父作用域上的函数绑定，从而以函数的方式调用controll中的函数。