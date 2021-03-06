运算符重载的主要优点就是允许改变使用于系统内部的运算符的操作方式，以适应用户自定义类型的类似运算。

- C++中的运算符除了少数几个之外，全部可以重载，而且只能重载C++中已有的运算符。

```
算术运算符：+, -, *, /, %, ++, --;
位操作运算符：&, |, ~, ^, ＜＜, ＞＞
逻辑运算符：!, &&, ||;
比较运算符：＜, ＞, ＞=, ＜=, ==, !=;
赋值运算符：=, +=, -=, *=, /=, %=, &=, |=, ^=, ＜＜=, ＞＞=;
其他运算符：[], (), -＞, ,(逗号运算符), new, delete, new[], delete[], -＞*。
不允许重载：., *, ::, ?:, sizeof
```

- 重载之后运算符的优先级和结合性都不会改变。对运算符重载不改变运算符的优先级和结合性，并且运算符重载后，也不改变运算符的语法结构，即单目运算符只能重载为单目运算符，双目运算符只能重载双目运算符。

- 运算符重载是针对新类型数据的实际需要，对原有运算符进行适当的改造。一般来说，重载的功能应当与原有功能相类似，不能改变原运算符的操作对象个数，同时至少要有一个操作对象是自定义类型。
- 运算符重载实际是一个函数，所以运算符的重载实际上是函数的重载。编译程序对运算符重载的选择，遵循着函数重载的选择原则。
- 运算符重载形式有两种，重载为类的成员函数和重载为类的友元函数。

运算符重载为类的成员函数的一般语法形式为：
```
＜类名＞ operator ＜运算符＞(＜参数表＞)
{
  函数体；
}
运算符重载为类的友元函数的一般语法形式为：
friend ＜类名＞ operator ＜运算符＞(＜参数表＞)
{
  函数体；
}
```
其中，函数类型就是运算结果类型；operator是定义运算符重载函数的关键字；运算符是重载的运算符名称。

运算符重载为类的成员函数时，函数的参数个数比原来的操作个数要少一个；当重载为类的友元函数时，参数个数与原操作数个数相同。原因是重载为类的成员函数时，如果某个对象使用重载了的成员函数，自身的数据可以直接访问，就不需要再放在参数表中进行传递，少了的操作数就是该对象本身。

重载为友元函数时，友元函数对某个对象的数据进行操作，就必须通过该对象的名称来进行，因此使用到的参数都要进行传递，操作数的个数就不会有变化。有些运行符不能重载为友元函数，它们是：=, (), []和->。

**++/--运算符重载**，分为前置和后置两种，前置不带参数，后置带一个int参数(不使用)。
