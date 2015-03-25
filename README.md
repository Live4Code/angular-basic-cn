这个练习我们用指令来重构HTML的`button`元素，给原生的按钮控件换上新装。我们在HTML原生button的基础上用CSS来修饰，构建按钮指令。

这里要详细学习下指令的编译机制，即我们自定义的指令是怎么转换为页面上的控件的。指令的编译分为`compile`和`link`两个阶段。
对这两个阶段的理解对我们理解指令并写好指令至关重要。

### Compile

DOM的编译由`compile`执行。 它会遍历DOM并找到匹配的指令 (比如页面上所有的`<button></button>`，这里的button是我们自己定义的指令)，
然后指令中`compile`方法会调用。 compile可以修改DOM的内容，比如给按钮加上CSS类，生成`<button class="btn btn-primary"></button>`传给link函数。


### link

链接函数(`link`)来将模板与作用域(`$scope`)链接起来。就像控制器一样，指令也可以定义自己的$scope来实现双向绑定和动态更新。
指令的逻辑操作，和$scope中的变量的交互在这一步完成。至此指令的构建就大功告成，显示在页面上。