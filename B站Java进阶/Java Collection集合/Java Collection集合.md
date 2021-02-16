# Java Collection集合

## 一、集合概述

1.集合时java中提供的一种容器，可以用来存储多个数据。

2.集合和数组的区别：

- 数组的长度是固定的，而集合的长度是可变的。
- 数组中存储的是同一类型元素，既可以是基本类型元素也可以是引用对象元素。而集合中存储的都是==统一类型的引用对象元素==。

## 二、集合的架构

![image-20210215212912985](image-20210215212912985.png)

## 三、集合的区别与接口公共方法

![image-20210215213402049](image-20210215213402049.png)

![image-20210215214216362](image-20210215214216362.png)	

## 四、Iterator迭代器

1.作用：对 collection 进行迭代的迭代器。（对集合进行遍历）

2.方法：

![image-20210215215128003](image-20210215215128003.png)	

3.获取对象：

collection接口中有一个方法iterator( ),此方法用于返回的就是Iterator迭代器的实现对象。

```java
        //获取Iterator<>迭代器
        Iterator<String> iteratorStr = strings.iterator();
        //使用迭代器遍历输出集合
        while (iteratorStr.hasNext()){
            System.out.println(iteratorStr.next());
        }
```

