# 记事本
重新设置git bash的用户名和邮件地址
```
$  git config --global --replace-all user.email "输入你的邮箱"   
$  git config --global --replace-all user.name "输入你的用户名"
```
# 笔记   
一系列项目模板生成工具  
https://github.com/audreyr/cookiecutter  
GitHub操作指南  
https://github.com/tiimgreen/github-cheat-sheet/blob/master/README.zh-cn.md  
git冲突解决方法 官方文档   
https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/  
virtualbox运行失败解决方法  
1、https://www.cnblogs.com/xiaotao726/p/6506976.html  
2、将软件设置成兼容模式运行

scrapy安装报错  
下载对应python版本的Twisted的whl文件安装，然后再安装scrapy。  
下载地址：https://www.lfd.uci.edu/~gohlke/pythonlibs/#twisted  


运行scrapy crawl quotes报错 提示no module named "win32api"  

```
pip install pypiwin32
```  

网络爬虫的抓取策略  
https://ask.hellobi.com/blog/bixtcexs/11983  

爬虫利器Xpath
学爬虫利器XPath,看这一篇就够了  
https://zhuanlan.zhihu.com/p/29436838

# web通用测试用例
### 易用性
1、便于使用、理解、并能减少用户发生错误选择的可能性  
2、当数据字段过多时，使用便于用户迅速吸取信息的方式表现信息，突出重点信息，标红等方式  
3、显示与当前操作相关的信息，给出操作提示。  
4、界面要支持键盘自动浏览按钮功能，即按Tab键、回车键的自动切换功能  
5、对于常用的功能，用户不需要阅读用户手册就能使用  
### 一致性
1、是否符合广大用户使用同类软件的习惯  
2、表现形式的一致性，字体、按钮、控件风格、颜色、术语、提示信息等。(需要有一个全局的概念，不要每个模块都按照他们自己的风格做，结果每个模块效果做出来都不一致，这也是至关重要的所有要测试人员认真检查)  
3、交互习惯的一致性，查询、新增、编辑、删除等操作，并保证同一操作类型按钮名称一致。(顺序一致，页面位置也要尽量相同。)  
4、当输入框为不可输入或控件为不可使用状态时，统一为灰色不可输入状态;
### 有序性
1、界面文字、表单、图标等元素根据业务规则、使用频率排列  
2、Tab键的顺序与控件排列顺序要一致，目前流行总体从上到下，同时行间从左到右的方式  
3、必填项提示信息按照从上到下，从左到右的提示方式依次提示
### 安全性
1、ID/密码验证方式中能否使用简单密码。如密码标准为6位以上，字母和数字混合，不能包含ID，连续的字母或数字不能超过n位  
2、ID/密码验证方式中，连续数次输入错误密码后该账户是否被锁定  
3、不登录系统，直接输入登录后的页面的url是否可以访问，(添加拦截器)  
4、退出登录后按后退按钮能否访问之前的页面(确认在退出后他的session的信息被注销)  
5、当用户无意录入无效和不符合相关规范的数据(如电子邮箱就需要验证他的邮箱格式是否正确)时，并且给予提示信息  
6、在用户作出危险的选择时有信息进行提示，比如要删除系统的重要数据，或者这种操作可能对系统造成其他的影响  。
7、对可能引起致命错误或系统出错的输入字符或动作要加限制或屏蔽  
8、给用户提供UNDO功能用以撤销不期望的操作  
9、输入的特殊字符是否能正确处理：`~!@#$%^&*()_+-={}[]|:;”’ <>,./?
### 灵活性
1、用户能自由的作出选择，且选择都是可逆的  
2、用户方便的使用即互动多重性，不局限于单一的工具(包括鼠标、键盘或软键盘)  
3、当页面数据暴涨，出现较长列表时，是否有滚动条保证页面显示完整的信息。  
### 人性化
1、用户可依据自己的习惯定制界面，并能保存设置  
2、提供常用的快捷方式  
3、尽量减少用户输入动作的数量，加快输入的速度:例如,日期等可以提供默认显示当天日期并且可以进行清除和选择日期，下拉默认选中“请选择”，单选框默认选取使用频率最高的选项等  
4、是否用合理的最少步骤实现常用的操作，获得高效率  
5、是否提供进度条、动画等反映正在进行的比较耗时间的过程，(特别有的操作可能造成长时间等待，没有直观的呈现出现在的操作状态或相关的提示信息，容易让不熟悉系统的人误会系统出现了问题)  
6、是否为重要的操作返回必要的结果信息如：成功，失败(失败的原因)，正在执行
7、重要的对象是否用醒目的色彩表示，  
8、色彩使用是否符合行业的习惯，界面的色调是否让人感到和谐、满意
### 页面检查
1、界面布局有序，简洁，符合用户使用习惯  
2、界面元素是否在水平或者垂直方向对齐  
3、界面元素的尺寸是否合理  
4、行列间距是否保持一致  
5、是否恰当地利用窗体和控件的空白，以及分割线条  
6、窗口切换、移动、改变大小时，界面显示是否正常  
7、刷新后界面是否正常显示合理布局  
8、不同分辨率页面布局显示是否合理，整齐，分辨率一般为1024*768 > 1280*1024 >800*600  
9、不同的浏览器下渲染出来的页面是否存在变形的情况。
### 弹出窗口
1、弹出的窗口应垂直居中对齐  
2、对于弹出窗口界面内容较多，须提供自动全屏功能  
3、弹出窗口时应禁用主界面，保证用户使用的焦点  
4、活动窗体是否能够被反显加亮  
### 页面正确性
1、界面元素是否有错别字，或者措词含糊、逻辑混乱  
2、当用户选中了页面中的一个复选框，之后回退一个页面，再前进一个页面，复选框是否还处于选中状态  
3、导航显示正确  
4、title显示正确  
5、页面显示无乱码  
6、需要必填的控件，有必填提醒，如 *  
7、适时禁用功能按钮(如权限控制时无权限操作时按钮灰掉或不显示;无法输入的输入框disable掉)  
8、页面无js错  
9、鼠标无规则点击时是否会产生无法预料的结果  
10、鼠标有多个形状时是否能够被窗体识别(如漏斗状时窗体不接受输入)
### 控件检查
1、查询时默认显示全部  
2、选择时默认显示请选择  
3、禁用时样式置灰
### 复选框
1、多个复选框可以被同时选中  
2、多个复选框可以被部分选中  
3、多个复选框可以都不被选中  
4、逐一执行每个复选框的功能  
5、当复选框太多时，提供全选和全不选的功能
### 单选框
1、一组单选按钮不能同时选中，只能选中一个  
2、一组执行同一功能的单选按钮在初始状态时必须有一个被默认选中，不能同时为空
### 下拉树
1、应支持多选与单选  
2、禁用时样式置灰
### 树形
1、各层级用不同图标表示，最下层节点无加减号  
2、提供全部收起、全部展开功能  
3、如有需要提供搜索与右键功能，如提供需有提示信息  
4、展开时，内容刷新正常
### 日历控件
1、同时支持选择年月日、年月日时分秒规则  
2、打开日历控件时，默认显示当前日期  
### 滚动条控件
1、滚动条的长度根据显示信息的长度或宽度及时变换，这样有利于用户了解显示信息的位置和百分比，如，word中浏览100页文档，浏览到50页时，滚动条位置应处于中间  
2、拖动滚动条，检查屏幕刷新情况，并查看是否有乱码  
3、单击滚动条时，页面信息是否正确显示  
4、用滚轮控制滚动条时，页面信息是否正确显示  
5、用滚动条的上下按钮时，页面信息是否正确显示
### 按钮
1、点击按钮是否正确响应操作。如单击确定，正确执行操作;单击取消，退出窗口  
2、对非法的输入或操作给出足够的提示说明  
3、对可能造成数据无法恢复的操作必须给出确认信息，给用户放弃选择的机会(如删除等危险操作)
### 文本框
1、输入正常的字母和数字  
2、输入已存在的文件的名称  
3、输入超长字符。  
4、输入默认值，空白，空格。  
5、若只允许输入字母，尝试输入数字;反之，尝试输入字母  
6、利用复制，粘贴等操作强制输入程序不允许的输入数据  
7、输入特殊字符集，例如，NUL及 等  
8、输入不符合格式的数据，检查程序是否正常校验，如程序要求输入年月日格式为yy/mm/dd，实际输入yyyy/mm/dd，程序应该给出错误提示。  
### 分页
1、当列表数据较多时是否使用分页控件。  
2、系统是否都是使用的同一风格的分页控件。  
### 上传功能检查
1、上传下载文件检查：上传下载文件的功能是否实现，上传下载的文件是否有格式、大小要求、是否屏蔽exe.bat.  
2、回车键检查:在输入结束后直接按回车键,看系统处理如何,会否报错。这个地方很有可能会出现错误  
3、刷新键检查：在Web系统中，使用浏览器的刷新键，看系统处理如何，会否报错。  
4、回退键检查：在Web系统中，使用浏览器的回退键，看系统处理如何，会否报错。对于需要用户验证的系统，在退出登录后，使用回退键，看系统处理如何;多次使用回退键，多次使用前进键，看系统如何处理。   5、直接URL链接检查：在Web系统中，直接输入各功能页面的URL地址，看系统如何处理，对于需要用户验证的系统更为重要。如果系统安全性设计的不好，直接输入各功能页面的URL地址，很有可能会正常打开页面。  
6、确认没有上传资料点上传按钮是否有提示  
7、确认是否支持图片上传  
8、确认是否支持压缩包上传  
9、若是图片，是否支持所有的格式(.jpeg,.jpg,.gif,.png等)  
10、音频文件的格式是否支持(mp3,wav,mid,等)  
11、各种格式的视频文件是否支持  
12、上传文件的大小有无限制，上传时间用户是否可接受?  
13、是否支持批量上传?  
14、若在传输过程中，网络中断时，页面显示什么  
15、选择文件后，想取消上传功能，是否有删除按钮  
16、文件上传结束后，是否有提示信息并且能回到原来界面  
### 添加功能检查
1、正确输入相关内容，包括必填项，点添加按钮，记录是否成功添加  
2、必填项内容不填、其它项正确输入，点添加按钮，系统是否有相应提示  
3、内容项中输入空格，点添加按钮，记录能否添加成功  
4、内容项中输入系统中不允许出现的字符、点添加按钮，系统是否有相应提示  
5、内容项中输入HTML脚本，点添加按钮，记录能否添加成功  
6、仅填写必填项，点添加按钮，记录能否添加成功  
7、添加记录失败时，原填写内容是否保存  
8、新添加的记录是否排列在首行  
9、重复提交相同记录，系统是否有相应提示  
### 删除功能检查
1、选择任意一条记录，进行删除，能否删除成功  
2、选择不连续多条记录，进行删除，能否删除成功  
3、选择连续多条记录，进行删除，能否删除成功  
4、能否进行批量删除操作  
5、删除时，系统是否有确认删除的提示
### 查询功能检查
1、针对单个查询条件进行查询，系统能否查询出相关记录  
2、针对多个查询条件，进行组合查询，系统能否查询出相关记录  
3、系统能否支持模糊查询  
4、查询条件全部匹配时，系统能否查询出相关记录  
5、查询条件全为空时，系统能否查询出相关记录  
6、查询条件中输入%，系统能否查询出相关记录  
7、系统是否支持回车查询  
8、系统是否设置了重置查询的功能



# 单词小记
extract 提取
