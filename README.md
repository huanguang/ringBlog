# ringBlog

ringBlog是一个基于Yii2的博客系统，提供最基础的的分类和博客功能。

【适用】
个人博客，初创公司官网，小团队主页
稍微懂一点技术，就可以快速定制自己的网站

【特点】
快速二次开发，可高度定制化，不重复学习新的规范。
安装和使用ringBlog不需要太多编程基础，但是二次开发需要一些PHP和前端经验，不推荐小白用户使用。
如果您是初学者，只需要按照下文的步骤安装，可以快速学习到git、composer、migration等先进的技术知识，有助于装逼。
如果您了解最基础的前端技术，可以轻易修改博客的样式，不需要重复学习如何开发主题模版。
如果您了解最基础的PHP，可以轻易地修改功能，不需要重复学习如何开发插件。
ringBlog使用大名鼎鼎的Yii2框架搭建，进行二次开发可以接触到最先进的PHP开发思想。

【准备工作】
确保你的服务器安装了PHP 5.4以上版本，推荐使用MySql数据库；
将域名解析到您的服务器，您需要准备两个二级域名：一个用于博客，一个用于后台管理。这能使博客更加安全；
确保服务器已经安装了composer（可以在Composer中文官网找到下载地址和安装方式）；
运行 composer global require "fxp/composer-asset-plugin:*" 来安装Composer Asset插件，Yii2 通过这个插件来安前端开发所用到依赖包；
确保服务器安装了git。

【安装流程】
在您服务器的 Web 访问目录下运行 "git clone https://github.com/oonne/ringBlog.git"。git会把ringBlog的源码自动下载到您的目录下；
打开 project目录下运行"composer install"。composer将帮您安装所需的插件和依赖；
运行 init 对系统进行初始化，在这一步您可以选择作为开发模式还是生产模式；
打开project/common/config目录，编辑main-local.php文件，填入您的数据库信息。您还可以通过修改params.php和params-local.php进一步修改您博客的设置；
在project目录下运行"php yii migrate/up"，这个命令将帮您初始化数据库；
在project/frontend/web目录下创建一个名为"uploads"的文件夹，该文件夹需要写入的权限（777）。您也可以修改project/backend/config/UEditor.json的配置，将上传图片和附件的文件夹改为其他路径；
访问您的博客后台，初始的帐号和密码是"admin"。
