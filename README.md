1.安装IIS服务器并打开：
win键搜索控制面板
!<image>(https://github.com/SuGar-456/UnityWebGL_IIS-local-deployment/blob/main/picture/ea9dae60-883e-4e94-822a-e0ab702cd4a9.png)




点击确定后开始下载安装IIS服务器

2.查找IIS服务器并打开：

3.配置IIS服务器：
选中网站右键点击添加网站 - 自定义名称



选择物理路径（一定要选择Build文件夹的父文件夹）



端口要选择一个未被占用的端口（CMD中使用netstat -ano查看端口）



点击确认后左侧会出现站点



4.为网站依次添加MIME类型:
选中后双击 MIME 类型



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
