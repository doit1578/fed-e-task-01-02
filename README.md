# fed-e-task-01-02



## 一

答：10

```javascript
// a[6]并没有保存当时的外部上下文中的i,当循环执行完成后，i变成10，故打印出10
a[6]=function(){
    console.log(i)
}
```



## 二

答：报错，if块中，let声明的变量不受外部影响，必须先声明，才能使用，否则报错



## 三

答：Math.min(...[arr]))



## 四

答：var 声明的变量，可以先使用后申明；let 声明的变量，只能在let命令所在的代码块内生效；const跟let相似，只是一旦声明后不能修改。



## 五

答：20，this在调用过程中，指向向上链式搜索过程中遇到的第一个function的调用者，而跟箭头函数无关



## 六

答：1、设置对象的私有属性；2、保证属性ID的唯一性



## 七

答：浅拷贝是拷贝的是对象的引用，而深拷贝是拷贝的对象本身



## 八

答：TypeScript是 JavaScript 的一个超集，提供了类型系统和对ES6的支持，可编译成纯 JavaScript，JavaScript是弱语言，在使用参数时，可以随意改动参数的类型，在使用的当时时非常爽的，但是后期维护就特别麻烦。



## 九

好处：
	增强代码的可读性和可维护性，强类型的系统相当于最好的文档，在编译时即可发现大部分的错误，增强编辑器的功能，完全支持 es6 规范。
缺点：
	增加学习成本，需要理解接口（Interfaces）和泛型（Generics），类（class），枚举类型（Enums），短期增加开发成本，增加类型定义，但减少维护成本，和有些库结合时不是很完美

## 十

答：引用计数器，是一个对象被引用的次数，每被引用一次，加一。优点是：垃圾回收快，停顿时间少。缺点是：对象如果是循环引用的化，会造成内存泄漏，而且还要单独维护计数器。



## 十一

答：标记整理算是，把堆内存分成A、B2个区域，程序根据可达性分析，标记没有被全局变量引用的对象或者闭包引用的并整理到A区域上，另一些被引用的整理到B区域上，然后一次性清除该内存区域A



## 十二

答：V8新生代采用的是复制算法，把内存区域分成from、to两块区域，当发生GC时，程序会把被全局变量引用的或者闭包引用的对象放入to中，然后清除from区域，再经历一轮GC存活的对象进入老生代



## 十三

答：增量标记算法V8提高清除效率优化时使用，工作原理是：在程序执行与增量标记交替进行，标记完成后与程序执行交替清除。
