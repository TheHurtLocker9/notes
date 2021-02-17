# Java 可变参数

1. 使用前提：

   - 当方法的参数列表数据类型已经确定，但参数的个数不确定时就可以使用可变参数，等同于==参数数组==。
   - JDK 1.5+

2. 使用格式：

   修饰符 返回值类型 方法名(数据类型 ... 变量名)｛｝

   ```java
   public class VariablePara {
       public static void main(String[] args) {
           System.out.println(sum());//0
           System.out.println(sum(1));//1
           System.out.println(sum(1,2));//3
           System.out.println(sum(1,2,3));//6
       }
   
       //可变参数本质上就是参数数组的便捷写法
       private static int sum(int ... arr) {
           int sum = 0;
           for (int i:arr) {
               sum+=i;
           }
           return sum;
       }
   }
   ```

3. 注意事项：

   - ==一个方法的参数列表，只能有一个可变参数！==
   - ==如果方法的参数有多个，那么可变参数必须写在参数列表的最后！==