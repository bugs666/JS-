# 1.	原始值包装类

Boolean，String，Number

# 2.	内置对象

Global，Window

1. Global对象

   ```
   js中最特别的内置对象，且没有提供可以显式访问这个对象的代码；在全局作用域中定义的变量和方法都会变成该对象的属性
   ```

2. Window对象

   ```
   浏览器中Global对象的代理，因此，在全局作用域中定义的变量和方法也会变成该对象的属性
   var color = ‘red’;console.log(window.color)//red
   ```

3. Math对象：提供了很多数运算的方法，取绝对值，取对数，取随机数等等