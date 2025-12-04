1.安装IIS服务器并打开：
win键搜索控制面板

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/7de91324-65f5-4d66-8091-05116a59f3de.png)

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/ea9dae60-883e-4e94-822a-e0ab702cd4a9.png)

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/9b23512b-5ca9-440a-9d40-fe8848d4dcec.png)

点击确定后开始下载安装IIS服务器


2.查找IIS服务器并打开：

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/836ddcbf-b579-4ab1-8614-86a801213947.png)

3.配置IIS服务器：

选中网站右键点击添加网站 - 自定义名称

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/b53bbf79-3751-495d-8c66-abe34a9c7b5d.png)


选择物理路径（一定要选择Build文件夹的父文件夹）

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/253f20a0-d953-4bb4-8fde-a5a578d7e6dd.png)

端口要选择一个未被占用的端口（CMD中使用netstat -ano查看端口）

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/50a8add4-3046-45bf-b20a-a7cf94e94e69.png)

点击确认后左侧会出现站点

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/3eae66e7-0258-4c5f-a42a-e1f0561678b3.png)

4.为网站依次添加MIME类型:
选中后双击 MIME 类型

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/ba14586e-1a79-40f3-ae55-ed31218c2025.png)

右上角添加

以下是Unity打包WebGL后时可能会用到的的相关类型，建议全部添加(前四个优先)

.unity3d

application/octet-stream

.unity3dgz

application/octet-stream

.unityweb

application/binary

.br

application/javascript

.mem

application/octet-stream

.data

application/octet-stream

.memgz

application/octet-stream

.datagz

application/octet-stream

.jsgz

application/x-javascript

5.添加跨越访问权限(可不配置)：

![Image text](https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/5e63f5d7-ee1b-4441-8c26-73fad2c22160.png)

相关HTTP响应头内容:

Access-Control-Allow-Origin

*

AcceIISwebss-Control-Allow-Methods

GET, POST, PUT, DELETE, OPTIONS

Access-Control-Allow-Headers

Content-Type

做完以上配置基本上就结束了
————————————————
版权声明：本文为CSDN博主「m0_58791145」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/m0_58791145/article/details/155560685
