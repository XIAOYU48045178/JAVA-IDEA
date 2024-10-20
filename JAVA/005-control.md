`control`
--

`分类 顺序控制 分支控制 循环控制`

`条件分支语句 IF`
--

```java
1、if(){...}

2、if(){...}else(){...}

3、if(){...}else if(){...}

4、if(){...}else if(){...}else{...}
```

`条件分支语句 Switch`
--

```java
switch(已知条件){
    case 常量 1:
        ...
        break;
    case 常量 2:
        ...
        break;
    default:
        ...
        break;
}
```

`表达式数据类型应和 case 后的常量类型一致 或者是可以自动转成可以相互比较的类型`

`表达式的返回值必须是 BYTE SHORT CHAR int ENUM String`

`case 中的值必须是常量而不能是变量`

`default 是可选的 当没有匹配的 case 时 执行 default`

`break 语句用来在执行完一个 case 分支后使程序跳出 switch 语句块 如果没有写 break 程序会顺序执行到 switch 结尾除非遇到break`

`IF VS Switch`
--

`对区间判断 对结果为 boolean 类型判断 使用 if if 的使用范围更广`

`循环语句 for`
--

```java
for(定义初始变量；条件判断；改变初始值){
    ...
}
```

`循环条件是返回一个布尔值的表达式`

`初始化和变量迭代可以写到其它地方但是两边的分号不能省略`

`循环初始值可以有多条初始化语句但要求类型一样并且中间用逗号隔开循环变量迭代也可以有多条变量迭代语句中间用逗号隔开`

`外层控行内层控列`

`> 9 x 9`

```java
public static void main(String[] args) {
    for(int i=1;i<10;i++) {
        for(int j=1;j<=i;j++) {
            System.out.print(j+"*"+i+"="+i*j+"\t");
        }
        System.out.println();
    }
}
```

`> 金字塔`

```java
public static void main(String[] args) {
    int totalLevel = 10;
    for (int i = 1; i <= totalLevel; i++) {
        for (int k = 1; k <= totalLevel - i; k++) {
            System.out.print(" ");
        }
        for (int j = 1; j <= 2 * i - 1; j++) {
            if (j == 1 || j == 2 * i - 1 || i == totalLevel) {
                System.out.print("*");
            } else {
                System.out.print(" ");
            }

        }
        System.out.println();
    }
}
```

`循环问题思路`
--

`化繁为简 即将复杂的需求 拆解成简单的需求 逐步完成` `先死后活 先考虑固定的值 然后转成可以灵活变化的值`

`循环语句 while`
--

```java
定义初始变量
while(条件){
    ...
    改变初始值
}
```

`循环语句 do while`
--

```java
定义初始变量
do{
    ...
    改变初始值
} while(条件)
```

`跳转控制语句 break`
--

`break 语句可以指定退出哪层循环 label 是标签名字由程序员指定 break 后指定到哪个 label 就退出到哪里 实际的开发中尽量不要使用标签如果没有指定 break 默认退出最近的循环体`

```java
public static void main(String[] args) {
    label1:
    for(int i = 0;i < 4;i++) {
        label2:
        for(int j = 0;j < 10;j++) {
            if(j == 2) {
                break label1;
            }
            System.out.println("j = " + j);
        }
    }
}
```

`跳转控制语句 continue`
--

`continue 语句用于结束本次循环 继续执行下一次循环 continue 语句出现在多层嵌套的循环语句体中时 可以通过标签指明要跳过的是哪一层循环`
