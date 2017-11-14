## 1.部署启动tomcat服务器 ##
1. 解压apache-tomcat-8.5.23-windows-x64.zip到一个非中文目录下
2. 配置环境变量，java_home（指向JDK安装的根目录）或jre_home
3. 双击apache-tomcat-8.5.23\bin目录下的startup.bat，启动服务器
4. 在浏览器中输入localhost：8080检验Tomcat安装是否正确
5. 若已经启动一个Tomcat应用，再启动同一个Tomcat应用会抛出异常：java.net.BindException:Address already in use:JVM_Bind:8080(端口已经被占用)

## 2.修改服务器端口 ##
修改server.xml 文件
<Connector port="8888" protocol="HTTP/1.1"
connectionTimeout="20000"
redirectport="8443"/>
把port的值改为其他端口号即可

## 3.启动Tomcat服务器##
1. cmd下
2. e: 回车
3. cd E:\apache-tomcat-8.5.23\bin
4. 启动 startup
5. 关闭 shutdown

## 4. 任意目录下启动Tomcat服务器##

