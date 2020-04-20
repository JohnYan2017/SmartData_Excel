##SMARTDATA数据处理工具

###能解决什么与EXCEL相关的问题:
- 当你需要对你的数据进行去空格,异常换行等可能影响数据质量的问题
- 当你需要对你的数据进行校验是否有异常(上下文字段格式不一致, 重复数据)
- 当你需要将复杂的表格(有透视表,图表,表格不规则,列转行)转化为标准表格
- 需要给系统或人员分享数据(针对某个表格或区域导出,而不是提供整个EXCEL)
- 需要对数据进行清洗,批量替换,合并,移除,计算..
- 你需要将非常多表格中相同表名的数据进行合并
- 你的表格中有非常多的数据,比如有一个字段是省, 你需要按省拆分出来数据分享
- 你需要链接数据库进行数据查询,下载到当前EXCEL的任意区域


###数据导出功能说明
适用于对手工EXCEL数据进行预处理清洗, 并导出供数据库或BI工具容易使用的CSV文件
本工具可以在不改变用户使用的表格, 实现数据的导出与上传, 而无需设计新的导入模版

大家应该都有这样的场景, 手上有一个表格, 可能会有很多页, 可能还有透视表, 图表等等, 这种表格一般是无法上传到数据库或供BI直接使用的.

我们可能会更希望能够**按需导出部分数据, 甚至可能需要进行列转行**, 或增加一栏导出时间, 或是转码, 自动去除左右空格, 或做数据校验
![](/media/editor/微信截图_20200412142720_20200412142828709663.png)
>以下说明可以因为版本的升级, 界面不太一致, 请参考对应

####针对无需进行列转行的数据:
操作技巧, 鼠标选择EXCEL所在单元格, 然后双击工具中"起始行","标题所在列","起始列"等的编辑框, 会自动填上当前所选单元格所在的行或列,而无需你去肉眼去数

起始行的选择, 可以让你更方便的导出增量数据或不规则的数据, 比如将一个表格中的150W条数据拆成3份导出, 你可以先将起始行设为100W, 然后导出,会将100W(含100w)行以下的数据导出, 然后将所选的这100W以下的数据临时删除,再把起始行设为50W, 导出, 再设为1 or 2 导出...
![](/media/editor/to_csv_20190710140753991574.png)

####针对列转行, 我们支持带多个表头,表头合并的单元格同样支持:
![](/media/editor/to_csv_2_20190717222359731116.png)

####编码转化
你可能有时想要用EXCEL打开导出的数据进行分析, 但你发现是乱码 或 目标系统需要指定编码格式, 所以我们支持多种导出编码供你选择

![](/media/editor/to_csv_code_20190717212814304357.png)

####数据校验
列转行时自动进行数值校验, 为你提前发现数据质量问题
![](/media/editor/微信截图_20200410112806_20200410113156216967.png)

支持基于上下文的数据类型校验, 可以校验数值或时间格式不一致的问题及错误值
![](/media/editor/微信截图_20200411121517_20200411122404350673.png)

####重复数据校验
勾选重复校验时, 如有重复数据会有如下提示, 你可以选择否,则不会导出此条重复记录, 当你再次点击取消时, 后续不再做提示, 对重复数据全部去重导出
此功能也可以用于做数据去重处理
![](/media/editor/微信截图_20200413091956_20200413092516090402.png)

####导出显示值
导出时默认是导出值, 比如时间的显示, 你可以用格式后显示是 XX年xx月, 但实际导出的会是值2020-04-12 14:30:00 之类, 如果你想要导出的是你所见的, 你可将此选项勾选

####增量控制
你可以通过修改  数据起始行, 结束行,起始列进行控制

####不想导出数据为空和0
当进行列转行时, 如果数据值为空或0, 一般情况下是没有意义的, 会增加数据量,所以数据值为空的都不会进行导出, 针到数据为0的, 默认是导出的, 如果你不想导出, 只需将含数据为0这个选项取消勾选

####保存上一次的配置
可能你有一个相同的表格要经常去进行导出, 我们会自动记忆你上一次的导出配置, 这样在下一次打开时会用自动使用上一次的配置, 你也可以点击 "重置" 恢复了默认配置



此工具当然不仅仅是这一个功能啦,我们还有:
>####合并表格:  支持一键合并当前文件夹(可以含子文件夹)下所有EXCEL文件
####拆分表格:  可以按照维度将表格中的数据拆分成多个表格
####文本处理:  支持批量去空格, 插入数据, 合并单元格数据等等
####下载数据:  建立数据库连接,便捷下载数据
####SQL工具:  支持一键生成建表语句,自动字段名转英文, 自动备注
更多功能请关注

###下载使用, 请点击 [数据处理工具](https://www.smartchart.cn/smartdata/download/ "数据处理工具")

###如果安装后打开无法开到图标或运行出错,请查看[安装问题](https://www.smartchart.cn/blog/article/2020/3/22/39.html "安装问题, 请查看")
