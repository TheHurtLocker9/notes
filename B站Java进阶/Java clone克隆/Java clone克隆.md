# Java clone克隆

## 克隆

clone克隆是创建对象的方法之一（==构造方法、对象的克隆、反序列化==）

1. 对象的克隆，Object类提供的克隆方法。它的修饰符是protected的，如果User对象想调用clone方法，==必须重该方法。==

   ```java
   //重写clone方法
      @Override
       protected Object clone() throws CloneNotSupportedException {
           return super.clone();
       }
   ```

   

2. 想要让对象支持克隆，需要==该对象的类实现一个接口Clonable接口==。只要该类实现该接口就可以了。==该接口是一个标记接口，没有抽象方法==，不需要去实现具体方法，实现接口就可以调用克隆方法。

   ```java
   public class User implements Cloneable{}
   ```

3. 克隆之后是新的地址值，产生了一个新的对象。

   ```java
   com.icss.User@1b6d3586
   com.icss.User@4554617c
   ```

## 深克隆与浅克隆

浅克隆对于对象中的==引用对象保持原对象的引用==，而深客隆对于对象中的==引用对象同样进行克隆==，在堆中为引用对象也开辟新的内存空间。

### 深克隆的实现：

1. 为克隆对象的引用对象==重写clone方法==并==实现Clonable标记接口==。
2. 在克隆对象中重写的clone方法中手动实现深克隆。

```java
//重写user的clone方法
@Override
protected Object clone() throws CloneNotSupportedException {
    //先把当前的user对象克隆
    User user = (User) super.clone();
    //将当前user对象的address属性克隆
    Address addr = (Address) user.getAddress().clone();
    //设置克隆之后的addr
    user.setAddress(addr);
    return user;
}
```

==备注：若子类与基类不在同一包中，那么在子类中，子类实例可以访问其从基类继承而来的protected方法，而不能访问基类实例的protected方法。== 可以联系private理解

