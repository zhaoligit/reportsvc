<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <title>欢迎使用《{服务名}》</title>
    <link rel="stylesheet" type="text/css" href="default.css">
    <style>
        table.helptab,
        table {
            border-collapse: collapse;
            width: 90%;
        }
        table.helptab ,table table {
            border: 0.1em solid rgba(236, 222, 222, 0.767);
        }
        tr {
            line-height: 30px;
        }

        table.helptab tr {
            line-height: 30px;
        }

        table.helptab tr td {
            text-align: left;
        }

        span.keyword {
            color: blue;
        }
        table.ptype{ 
            border-collapse: collapse;
            border: 0.1em solid rgba(236, 222, 222, 0.767);
            width: 60%;
        }
        table.ptype tr{ 
            border-collapse: collapse;
            border: 0.1em solid rgba(236, 222, 222, 0.767);
        }
        table.ptype .type1 td,table.ptype .type1{ 
            color:  rgba(65, 71, 71, 0.89);
        }
    </style>
</head>

<body>
    <a name="top"></a>
    <center>
        <h2 style="text-align: center;">《{服务名}》使用说明</h2>
    </center>
    <hr /> 
    <div style="position:absolute; bottom:4cm; right:1cm;font-size: xx-large;"><a href="#top">⇧</a></div>
    多维报表，这里是指通过将类似SQL的查询结果集，转换成具有复杂表头html table格式的工具。<br>
    根据实际使用场景，分别提供reportServer,和API形式的封装，同样地提供了Windows环境和Linux环境下的产品。
    <table class=ptype><tr class="type1"><td></td><td><a href="#API">API动态库</a></td>
        <td><a href="#reportServer">reportServer(HttpServer)</a></td></tr>
    <tr><td class="type1">Windows</td><td>Report4Java.dll</td><td>reportServer.exe</td></tr>
    <tr><td class="type1">Linux</td><td>libReport4Java.so</td><td>reportServer</td></tr>
</table>		
    
    &nbsp;&nbsp;本服务通过监听一个http端口提供服务。<br>
    &nbsp;&nbsp;请求端通过向服务端口POST UTF-8编码的数据，获取服务。
    <br>
    &nbsp;&nbsp;自动通过分隔字段将简单的二维表格，生成具有复杂表头的多维表格数据，以方便展示多维数据。
    <br>
    &nbsp;&nbsp;返回数据以json格式组织内容，{<span class="keyword">ret</span>:{<span
        class="keyword">GridFrame</span>:"row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]",
    <span class="keyword">Html</span>:"&lt;table&gt;...&lt;/table&gt;"}}
    <br>
    <h2>特色：</h2>
    <ol>
        <li>只需要通过常用的关系查询结果集，即可生成便于分析的多维表格。</li>
        <li>可以自动对中文序号进行排序处理，如星期一，二，三，...日；一月，二月，东南西北，上中下...</li>
        <li>可以指定表头内容，以及表头列顺序</li>
        <li>可以自动添加<span class="keyword">合计</span>项</li>
        <li>当需要通过数据原有顺序来决定展示顺序时，请不要指定<span class="keyword">行排序</span></li>
    </ol>

    <hr /> 
    <table class="helptab" border="1">
        <tr style="background-color:#6289f5;">
            <th>参数</th>
            <th>说明</th>
        </tr>
        <tr>
            <td>Csvdata</td>
            <td>带有字段名称行的csv文本格式，以<span class="keyword">\t</span>分隔字段,以<span class="keyword">\n</span>分隔记录，以<span
                    class="keyword">|</span>分隔行列字段</td>
        </tr>
        <tr>
            <td>Separate</td>
            <td>分隔字段，如：<span class="keyword">|，||，$</span>,默认为<span class="keyword">|</span></td>
        </tr>
        <tr>
            <td>Measures</td>
            <td>指定指标字段，如：<span class="keyword">IMSI个数,设备数</span></td>
        </tr>
        <tr>
            <td>GridFrame</td>
            <td>指定表头格式内容。<br>
                仅允许调整同一行的成员顺序，不同行的顺序请通过csv格式的数据列顺序来调整。<br>
                如：<span
                    class="keyword">row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]</span>
            </td>
        </tr>
        <tr>
            <td>SumOption</td>
            <td>
                <table border="1">
                    <caption>合计处理策略</caption>
                    <tr>
                        <td style="width: 20%;">SumNone</td>
                        <td>不自动加合计<br>
                            当数据中已经含有【合计】时，或者不需要展示【合计】时</td>
                    </tr>
                    <tr>
                        <td>SumIncRow</td>
                        <td>自动加行合计</td>
                    </tr>
                    <tr>
                        <td>SumIncCol</td>
                        <td>自动加列合计</td>
                    </tr>
                    <tr>
                        <td>SumIncRowCol</td>
                        <td>自动加行和列的合计</td>
                    </tr>
                </table>
            </td>
        </tr>
        <tr>
            <td>SumPos</td>
            <td>
                <table border="1">
                    <caption>合计位置策略</caption>
                    <tr>
                        <td style="width: 20%;">SumFirst</td>
                        <td>合计排在前面</td>
                    </tr>
                    <tr>
                        <td>SumLast</td>
                        <td>合计拓在后面</td>
                    </tr>
                </table>
            </td>
        </tr>
        <tr>
            <td>RowColSort</td>
            <td>
                <table border="1">
                    <caption>成员顺序策略</caption>
                    <tr>
                        <td style="width: 20%;">SortColMbr</td>
                        <td>默认对列成员排序。<br>仅当<span class="keyword">GridFrame</span>为空时起作用，<span
                                class="keyword">GridFrame</span>不为空时，由<span class="keyword">GridFrame</span>指定列顺序</td>
                    </tr>
                    <tr>
                        <td>SortRowMbr</td>
                        <td>对行成员排序</td>
                    </tr>
                </table>
            </td>
        </tr>
        <tr style="background-color: cornflowerblue;">
            <td colspan=2>POST后的返回值json格式
            </td>
        </tr>
        <tr>
            <td>ret</td>
            <td>
                <table border="1">
                    <tr>
                        <td colspan=2>
                            {ret:{GridFrame:"row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]",
                            Html:"&lt;table&gt;...&lt;/table&gt;"}}
                        </td>
                    </tr>
                    <tr>
                        <td style="width: 20%;">GridFrame</td>
                        <td>row:[IMSI,日期],col:[IMSI个数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]],设备数[星期一[东面,南面,西面,北面],星期三[南面,北面],星期日[南面]]]
                        </td>
                    </tr>
                    <tr>
                        <td>Html</td>
                        <td>&lt;table&gt;...&lt;/table&gt;</td>
                    </tr>
                </table>
            </td>
        </tr>
    </table>
    <hr /> 
    <pre>
        $.post({
            url : "http://ip:1024/Report",
            contentType : "application/x-www-form-urlencoded",
            data : "<span class="keyword">Csvdata</span>=IMSI%09日期%09||%09IMSI个数%09设备数%09星期%09分类名%0A"\
            "460070633324801%092020-03-01%09||%091%091%09星期一%09北面%0A"\
            "460070633324801%092020-03-02%09||%091%091%09星期一%09南面"\
            "&<span class="keyword">Separate</span>=||&<span class="keyword">Measures</span>=IMSI个数,设备数&<span class="keyword">SumOption</span>=SumIncRowCol&<span class="keyword">SumPos</span>=SumFirst&<span class="keyword">RowColSort</span>=SortRowMbr",
            //成功后的方法
            success : function(msg) {
                $("textarea[name='GridFrame']").val(msg.ret.GridFrame);
                $("#div1").html(msg.ret.Html);
            }
        });

    </pre>
    <hr /> 
    <h4><a name="API">报表API的使用</a></h4>
<pre>
    在Windows中，将Report4Java.dll拷贝到环境变量PATH能够搜索的位置。
    在Linux中，将libReport4Java.so拷贝到环境变量LD_LIBRARY_PATH能够搜索的位置。
    同样的，要求授权文件(license.lic)也拷贝到相应位置。
    通过授权页面获取授权信息后，授权文件(license.lic)将会自动保存在相应的服务程序目录：reportServer.exe(或reportServer)所在目录。
</pre>
<hr /> 
    <h4><a name="reportServer">reportServer的安装与运行</a></h4>
<pre>
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
</body>

</html>
