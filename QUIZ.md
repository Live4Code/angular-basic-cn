继续我们复仇者之战中的演员角色的例子。

我们来实现下ng-repeat中控制排序的方向。在**main.js**41行定义了$scope.reverse变量来控制排序方向。**index.html**中第22行提示了用法```orderBy:attr:reverse```,
`orderBy`过滤器可以串联要排列的属性，以及排序的方向。当reverse为true时是按照从大到小排列，reverse不存在或为false时，排序的顺序是从小到大。

请在**index.html**中第23行和24行中ng-click上加上反转$scope.reverse的代码，使得点击同一属性可以反转以该属性排序的方向。