#代码性能调整技术


###逻辑

* 在知道答案后停止判断
* 按照出现频率调整判断顺序
* 使用惰性求值

###循环

* 判断外提
* 尽可能减少在循环内部做的工作
* 用哨兵值替代符合判断
* 把最忙的循环放在最内层

###数据变换

* 使用整形数而不是浮点数
* 数组维度尽可能少
* 使用辅助索引
* 使用缓存机制

###表达式

* 利用代数恒等式，用低代价操作替代复杂操作。ex：要判断sqrt(x)<sqrt(y)先判断x<y
* 削弱运算强度。ex：加代替乘，移位代替乘2、除2
* 预先计算：编译期初始化，执行前存入文件，启动时计算之后引用，循环开始前计算，第一次需要结果时计算并保存备后用

###子程序

* 将子程序重写为内联
