# JOSM安装教程

***

## 前言

* **注意**，打开这些网站都需要使用魔法！

* JOSM（Java OpenStreetMap Editor）是一个开源的地图编辑器，用于编辑OpenStreetMap（OSM）数据。它允许用户查看、编辑和上传地理数据，以改善和扩展`OSM`地图。

* 首先我们在地图文件的下载网站（[https://www.openstreetmap.org/](https://www.openstreetmap.org/)）中下载好我们所需要的`map.osm`文件，最好更改一下名称方便后续使用，如重名名`GDUT_map.osm`。

+ 在下载好`osm`文件后，我们在虚拟机中查看如果有部分线路达不到预期所要的范围，有些道路会延伸出很长一段，不易查看，如图所示预期地图大小：

![alt GDUT地图](Image/期望道路大小.png)

+ 但是在实际的虚拟机中查看的地图：

![alt 需要修改的地图](Image/多线路.png)

+ 所以，我们需要利用到JOSM软件工具，对`osm`文件进行修改，删去（或者添加）部分道路。

## JSOM安装方法

1. 首先，我们需要在JOSM软件下载网站（[https://josm.openstreetmap.de/](https://josm.openstreetmap.de/)）下载Windows版本的文件，按照图片所示点击下载Windows版本的EXE文件：

![alt 下载地址](Image/下载网址.png)

下载好之后在文件夹中打开，点击右键**以管理员身份运行**，如果安装没有问题，则桌面会直接出现JOSM软件的快捷方式，后面打开JOSM软件，在左上角点击 `文件→打开→选择需要修改的osm文件` ，之后对打开的`osm`文件进行修改编辑，后面保存好后，`osm`地图文件就顺利修改完成了。
在JSOM中查看修改后的地图：

![alt 修改后的地图](Image/修改后的地图.png)

2. 在对osm文件编辑之后我们需要重新将该osm文件拉进虚拟机中，重新生成一下三个文件
（**可以将之前虚拟机中的这些文件删除，重新来一遍步骤，这样更方便**）

    >***.net.xml文件：路网构建、创建交通信号灯等，生成道路文件；

    >***.rou.xml文件：生成车辆文件；

    >***.sumocfg文件：将net.xml和rou.xml文件结合起来实现仿真。

重新来一遍过程之后，虚拟机中的地图就应该是预期所希望的大小了。

3. 如果安装失败，出现这个类似的问题警告：

![alt 安装Java](Image/安装Java.png)

在出现`Verify that you have access to that directory.`问题时，就是电脑没有安装Java，解决办法就是安装好Java就行，Java官网连接（[https://www.java.com/zh-CN/](https://www.java.com/zh-CN/)）。

4. 如果安装继续出现这样的问题：

![alt 关闭杀毒软件](Image/关杀毒软件.png)

解决办法就是**关闭杀毒软件！** 比如360、电脑管家等。
