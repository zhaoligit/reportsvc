# reportsvc
《报表服务》使用说明
<pre>
⇧多维报表，这里是指通过将类似SQL的查询结果集，转换成具有复杂表头html table格式的工具。
根据实际使用场景，分别提供reportServer,和API形式的封装，同样地提供了Windows环境和Linux环境下的产品。
API动态库	reportServer(HttpServer)
Windows	Report4Java.dll	reportServer.exe
Linux	libReport4Java.so	reportServer
  本服务通过监听一个http端口提供服务。
  请求端通过向服务端口POST UTF-8编码的数据，获取服务。
  自动通过分隔字段将简单的二维表格，生成具有复杂表头的多维表格数据，以方便展示多维数据。
  返回数据以json格式组织内容，{ret:{GridFrame:"row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]", Html:"<table>...</table>"}}
特色：
只需要通过常用的关系查询结果集，即可生成便于分析的多维表格。
可以自动对中文序号进行排序处理，如星期一，二，三，...日；一月，二月，东南西北，上中下...
可以指定表头内容，以及表头列顺序
可以自动添加合计项
当需要通过数据原有顺序来决定展示顺序时，请不要指定行排序
参数	说明
Csvdata	带有字段名称行的csv文本格式，以\t分隔字段,以\n分隔记录，以|分隔行列字段
Separate	分隔字段，如：|，||，$,默认为|
Measures	指定指标字段，如：IMSI个数,设备数
GridFrame	指定表头格式内容。
仅允许调整同一行的成员顺序，不同行的顺序请通过csv格式的数据列顺序来调整。
如：row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]
SumOption	
合计处理策略
SumNone	不自动加合计
当数据中已经含有【合计】时，或者不需要展示【合计】时
SumIncRow	自动加行合计
SumIncCol	自动加列合计
SumIncRowCol	自动加行和列的合计
SumPos	
合计位置策略
SumFirst	合计排在前面
SumLast	合计拓在后面
RowColSort	
成员顺序策略
SortColMbr	默认对列成员排序。
仅当GridFrame为空时起作用，GridFrame不为空时，由GridFrame指定列顺序
SortRowMbr	对行成员排序
POST后的返回值json格式
ret	
{ret:{GridFrame:"row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]", Html:"<table>...</table>"}}
GridFrame	row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]
Html	<table>...</table>
        $.post({
            url : "http://ip:1024/Report",
            contentType : "application/x-www-form-urlencoded",
            data : "Csvdata=IMSI%09日期%09||%09IMSI个数%09设备数%09星期%09分类名%0A"\
            "460070633324801%092020-03-01%09||%091%091%09星期一%09北面%0A"\
            "460070633324801%092020-03-02%09||%091%091%09星期一%09南面"\
            "&Separate=||&Measures=IMSI个数,设备数&SumOption=SumIncRowCol&SumPos=SumFirst&RowColSort=SortRowMbr",
            //成功后的方法
            success : function(msg) {
                $("textarea[name='GridFrame']").val(msg.ret.GridFrame);
                $("#div1").html(msg.ret.Html);
            }
        });

    
报表API的使用
    在Windows中，将Report4Java.dll拷贝到环境变量PATH能够搜索的位置。
    在Linux中，将libReport4Java.so拷贝到环境变量LD_LIBRARY_PATH能够搜索的位置。
    同样的，要求授权文件(license.lic)也拷贝到相应位置。
    通过授权页面获取授权信息后，授权文件(license.lic)将会自动保存在相应的服务程序目录：reportServer.exe(或reportServer)所在目录。
reportServer的安装与运行
    将reportserver.zip或reportserver.tar解压，然后运行即可。
    两个压缩文件内容相同，仅压缩打包方式不同。
解压：
    unzip reportserver.zip -d .
 或 tar -xvf reportserver.tar 
运行：
Windows:
	在cmd窗口，根据需要，执行以下命令。
	reportServer.exe 1024 -d		(即时运行一次，关闭后即退出)
	reportServer.exe 1024 -i		(安装为Windows服务，服务名为ReportServer1024，这个需要管理员权限)
Linux:
	类似Windows，在shell下，根据需要执行以下命令。
	./reportServer  1024 -d		(即时运行一次，关闭后即退出)
	./reportServer  1024 	    (以守护进程方式运行)
</pre>
