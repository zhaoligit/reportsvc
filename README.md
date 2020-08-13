# 欢迎使用《报表服务》
报表服务

[查看安装使用说明]( https://htmlpreview.github.io/?https://github.com/zhaoligit/reportsvc/blob/master/index.html)  
通过SQL查询结果集生成复杂多维表格,有中文成员排序,可自定义列头顺序.  
[查看版权信息]( https://htmlpreview.github.io/?https://github.com/zhaoligit/reportsvc/blob/master/copyright.html)  

## 下载
 [reportserver.tar](https://github.com/zhaoligit/reportsvc/raw/master/reportserver.tar) tar格式的打包文件  
 [reportserver.zip](https://github.com/zhaoligit/reportsvc/raw/master/reportServer.zip) zip格式的打包文件  
 [webApp.zip](https://github.com/zhaoligit/reportsvc/raw/master/webApp.zip)  报表API调用例子  

![图片](https://github.com/zhaoligit/reportsvc/raw/master/demotab.jpg "示例图片")

　　　　|     API动态库     |报表服务(HttpServer)  
---------|-------------------|-----------------  
Windows	|Report4Java.dll    |reportServer.exe  
Linux  	|libReport4Java.so  |reportServer  

## 特色：
1. 只需要通过常用的关系查询结果集，即可生成便于分析的多维表格。
1. 可以自动对中文序号进行排序处理，如星期一，二，三，...日；一月，二月，东南西北，上中下...
1. 可以指定表头内容，以及表头列顺序
1. 可以自动添加合计项
1. 当需要通过数据原有顺序来决定展示顺序时，请不要指定行排序
## reportServer的安装与运行  
    将reportserver.zip或reportserver.tar解压，然后运行即可。  
    两个压缩文件内容相同，仅压缩打包方式不同。  
### 解压：
    unzip reportserver.zip -d .  
    或 tar -xvf reportserver.tar   
### 运行：(然后通过 http://127.0.0.1:1024 即可访问)
>Windows:  
>>在cmd窗口，根据需要，执行以下命令。  
>>reportServer.exe 1024 -d		(即时运行一次，关闭后即退出)  
>>reportServer.exe 1024 -i		(安装为Windows服务，服务名为ReportServer1024，这个需要管理员权限)  

>Linux:  
>>类似Windows，在shell下，根据需要执行以下命令。  
>>./reportServer  1024 -d		(即时运行一次，关闭后即退出)  
>>./reportServer  1024 	    (以守护进程方式运行)  
