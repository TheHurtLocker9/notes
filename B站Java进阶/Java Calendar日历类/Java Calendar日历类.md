# Java Calendar日历类

## 一、介绍

java.util.Scanner是一个日历抽象类，其中提供了操作日历字段的方法，日常多使用其子实现类GregorianCalendar类。

## 二、对象的创建和使用

1.与其他语言环境敏感类一样，`Calendar` 提供了一个类方法  `getInstance`，以获得此类型的一个通用的GregorianCalendar对象。

> ```java
> Calendar rightNow = Calendar.getInstance();
> ```

2.方法：get()、set()、add()、getTime()等

```
int year = rightNow.get(Calendar.Year);
```

