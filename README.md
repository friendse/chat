# chat
一. WeLive介绍：
    ------------------
    WeLive在线客服系统是一个程序小巧, 安装使用简单的网上在线客服系统, 主要特点：

   1. 基于PHP + MySQL + Ajax技术的在线客服系统;
   2. 用户安装在自己的服务器或虚拟主机, 安装一次可在任意网站或页面中调用;
   3. 前台中英文双语, 根据用户浏览器的语言自动切换或由管理员设置指定;
   4. 客服人员多窗口与不同的访客同时交流;
   5. 客服人员分组管理, 无限制添加客服人员;
   6. 新信息窗口闪动, 信息提示声音, 颜色, 表情符号等等。

==============================================================

二. WeLive安装：
    ------------------
  A. 系统要求:
  --------------
    1. Unix, Linux或Windows Web服务器, 要求支持Ajax.
    2. PHP4.1或以上.
    3. MySQL4.0或以上.
 

  B. 安装步骤:
  --------------
    1. 设置FTP上传工具的传送模式为"二进制", 否则上传的PHP程序可能会在运行时发生意想不到的错误.
        如设置FlashFXP：选项 -> 参数设置 -> 打开对话框 -> 传送 -> 在传送模式中选择"二进制(图像)"
 
    2. 解压程序包后, 使用FTP工具上传到网站服务器某一指定目录如: welive/

    3. linux或unix服务器需要更改以下文件夹或文件属性为可写:

       ./welive/cache/                      属性: 777
       ./welive/config/                     属性: 777
       ./welive/config/settings.php         属性: 777


    4. 新建一个MySQL数据库或向虚拟主机服务商索取已存在的MySQL数据库的数据库名, 用户名, 用户密码信息。

    5. 在浏览器中输入地址: http://www.xxxx.com/welive/install/, 系统提示安装.
       安装完成后建议删除安装目录 ./welive/install/


  C. 重新安装:
  -------------
    1. 重新安装需要删除./welive/config/config.php文件, 上传install文件夹, 然后按第B.5步安装.
        
==============================================================

三. WeLive使用：
    ------------------
    WeLive系统使用非常简单, 登录闻泰论坛可查阅更多相关使用方面的文章. 
    
    1.  调用客服小面板(浮动):
    -------------------------
       a. html文件中调用代码: 
           <script src="http://www.xxxx.com/welive/welive.php" language="javascript"></script>

           在html文件中的<head></head>或<body></body>之间插入上面一行代码, 网页就能调用客服小面板.

	   注意: 上面的文件地址为绝对地址, 当然也可以使用相对地址, 
	   但如果您不知道当前html文件和welive.php的相对关系, 那么使用绝对地址将更为简单方便.

       b. php文件中调用: 
           在任何php代码段添加下面一句: 
	   echo '<script src="http://www.xxxx.com/welive/welive.php" language="javascript"></script>';

	   或在php文件中的html代码段添加下面一句: 
	   <script src="http://www.xxxx.com/welive/welive.php" language="javascript"></script>

       c. 在weenCompany企业网站系统中调用:
           如果希望在weenCompany系统的任何页面中都显示客服小面板, 可打开weenCompany的index.php文件: 
	   查找到这一句:

	   <script type="text/javascript" src="includes/javascript/hovermenu/menu.js"></script>';

	   在其后面添加并变为如下(注意语句结尾的标点符号):

	   <script type="text/javascript" src="includes/javascript/hovermenu/menu.js"></script>
	   <script src="http://www.xxxx.com/welive/welive.php" language="javascript" ></script>';
 
           如果希望仅在weenCompany系统的某个模板样式中显示客服小面板, 可打开这个模板样式文件: 
	   在此样式文件的</head>之前添加下面一句:
	   <script src="http://www.xxxx.com/welive/welive.php" language="javascript"></script>

	d. 在其它编程语言(如ASP)编写的网页文件中均调用显示客服小面板, 参考以上说明或访问闻泰论坛提问.


    2.  直接在页面中插入客服图片(固定):
    ------------------------------------
        在需要显示WeLive在线客服系统“客服图片”的页面<body></body>之间任意您需要的地方,
        插入以下代码：

        <script src="http://www.xxxx.com/welive/welive_image.php" language="javascript"></script>

        注：a.  四个客服在线状态图片存放在images目录, 可以随意更换, 但不要改名;
            b.  客服在线状态图片无法显示QQ, MSN, Skype的在线状态;

 
    3.  管理员及客服人员登录:
    -----------------------------
       a. 管理员及客服人员的操作面板登录地址为: http://www.xxxx.com/welive/

       b. 建议修改客服人员的登录名和密码: 
          系统默认安装后, 系统自带客服人员的登录密码都与管理员密码相同, 请自行修改, 删除或添加.

       c. 只有管服人员登录后，系统才可以提供在线服务.
