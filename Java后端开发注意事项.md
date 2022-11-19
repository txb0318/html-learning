### Java后端开发注意事项

异常处理

1. try-catch-finally
   
   ```java
   try
   {
       //代码可能存在异常
   }
   catch(Exception exception)
   {
       //捕获异常
       //1.异常发生时，系统将异常封装成Exception对象exception
       //2.传值给catch
       //3.获取异常对象时，程序员自己处理
       //4.若try中代码无异常，则catch不会发生
   }
   finally
   {
       //1.无论try中代码是否存在异常，始终执行finally    
       //2.通常将释放资源的代码，放在finally关闭
   }
   ```

2. throws

> main方法由JVM调用，main方法调用 f1 方法，f1 方法调用 f2 方法，如果 f2 方法发生异常，有两种方案，分别是 try-catch-finally 和 throws ，f2 使用 throws 方法，返回给 f1，f1也可以同样选择throws方法，返回给 main 方法，最终返回到 JVM。而 JVM 对处理异常的发生极为粗暴（1.输出异常信息。2. 退出程序）。

- [x] 
