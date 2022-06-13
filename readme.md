
## 项目目录结构
```
HqWebHello
----src
-------HelloServlet.java
----WEN-INF
-----------classes
------------------HelloServlet.class
-----------lib
--------------servlet-api.jar等
-----------web.xml
----index.html
```


## 在tomcat的server.xml的host节点配置自己项目的虚拟目录
例如
```
<host>
	<!--配置自己的项目路径-->
 	<Context path="/hello" docBase="/Users/hehuiqi/Desktop/HqWebHello" reloadable="true">
        </Context>
</host>
path="/hello" 虚拟路径
docBase="/Users/hehuiqi/Desktop/Hello" 项目真实路径
reloadable="true" true表示在不重启tomcat的情况下自动重新载入class文件
```

## 编译java源文件

```
# -sourcepath 指定java源文件路径 -d 指定生成class文件的路径

javac -sourcepath -d 

```
例如：
```
javac -sourcepath ./src/ ./src/*.java   -d ./WEB-INF/classes/
```

## 测试
注意自己的servlet配置路径在 web.xml <url-pattern>
输入 

http://127.0.0.1:8080/hello

或

http://127.0.0.1:8080/hello/servlet/HelloServlet






