# Java String详解

1. ###### 字符串的创建

   ![image-20210201111720197](image-20210201111720197.png)

2. ###### 字符串常量池：String字符串指向堆中常量池里的字符串对象，而常量池中字符串对象存储的是堆中的byte字节数组的地址。（字符串底层均以byte字节数组的形式存储）

   ![image-20210201112508140](image-20210201112508140.png)

3. ###### 字符串的比较：

   1. ==基本类型比较数值，引用类型比较地址值。
   2. equals(Object obj)  当参数是字符串且内容相同时返回true，否则返回false。
   3. equalsIgnoreCase(String str) 忽略大小写比较两字符串。 

4. ###### 字符串的常用方法

   ![image-20210201123441871](image-20210201123441871.png)

   ![image-20210201123909904](image-20210201123909904.png)

   ![image-20210201125457664](image-20210201125457664.png)

   ![image-20210201130132279](image-20210201130132279.png)

   