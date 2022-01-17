# Html中的js,script标签

通过使用'<script>'标签，可以在html文件中嵌入js脚本，该标签有8个属性设置：

1. async属性：

   ```
   该属性是一个可选属性，只对外部脚本生效，表示立即开始下载脚本资源，但是不影响页面的其他动作;
   当页面需要加载多个异步脚本时，浏览器不会保证按照脚本出现的顺序进行加载
   ```

2. charset属性：设置脚本的字符编码，只适用于外部脚本

3. defer属性：

   ```
   表明脚本在页面加载完成解析之后再执行，只适用于外部脚本;
   该属性可以保证脚本的加载顺序是脚本出现的顺序;
   ```

4. src属性：

   ```
   要加载的外部脚本的路径，只适用于外部脚本;浏览器解析这个脚本资源的时候，会向src指定的路径发送一个get请求来获取资源
   ```

5. type属性：用来设置脚本的语言类型，通常为text/javascript
   

除了使用标签的方式，还可以通过DOM（文档对象模型）API动态加载脚本


   ```
   let script = document.createElement('script');
   script.async = false;
   script.src = 'index.js';
   document.head.appendChild(script);
   ```

