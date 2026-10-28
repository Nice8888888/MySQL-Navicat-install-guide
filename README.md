# MySQL-Navicat-install-guide
Windows 11 下 MySQL 与 Navicat 的安装配置记录
# Windows 11 安装 MySQL 与 Navicat：过程记录

这篇文章记录我在 Windows 11（Intel处理器） 上安装 MySQL 和 Navicat、
配置本地数据库连接的过程，以及安装过程中遇到的问题。

## 一、电脑环境

- 操作系统：Windows 11
- 处理器：Intel 第 13 代 Core i7
- MySQL 版本：待安装完成后填写
- Navicat 版本：Navicat Premium 18
- Navicat 授权：学生非商业订阅

如果你是在校学生或者是老师，可以申请Navicat官方主页的“Navicat学术伙伴计划”![Navicat 学术伙伴计划申请入口](Navicat学术伙伴计划.png)，免费使用指定时间、指定版本的Navicat官方软件。如果是学生的话，可以先填写官网的资料，记得最好使用学校邮箱，便于后续审核。填写完毕后，邮箱会受到官方邮件，要求你填写指定表格并且提供学信网含二维码的在读证明。按要求发过去之后大概一天就会审核通过，告知你如何激活Navicat订阅，会给出详细网址和步骤。
## 二、下载安装包

### 1. 下载 MySQL

大家可以直接打开MySQL官网(https://www.mysql.com/cn/)，下拉到该网页底部，寻找“下载”字样，选择“MySQL Community Sever”，点击进去就会出现界面![MySQL 版本选择与安装包下载页面](mysql_download.png),大家根据需要选择是和半版本就可以，我这里选择的是8.4.13。大家选择好版本以后一定记得看下这里下载入口这里的版本号是否正确，因为可能会出现版本号未更新的情况。核对完就可以点击第一个下载入口，就是MSI Installer这里。之后进入以下界面![跳过 Oracle 账号登录，直接下载 MySQL](download.png),这里可以选择点击最下面的蓝色字体“No thanks,just start my download”进行安装。安装可能会花费几分钟时间。

### 2. 下载 Navicat

你可以按照邮件里面的网址自由选择需要的版本进行安装，这里我使用的是
Navicat Premium - Non-Commercial Simplified Chinese Edition，网址为
(https://www.navicat.com.cn/download/navicat-premium)，
直接点击就可以打开对应的下载界面![Navicat Premium Windows 64 位下载入口](Navicat_download.png)。里面会显示三个下载位置，位置1和位置2是同一产品的不同下载入口，第一个下载慢或失败时换第二个。我是用了VPN，所以下载的还比较快。

## 三、安装与配置 MySQL

安装完毕后打开会出现以下界面![MySQL 安装向导欢迎页面](mysql1.png)，直接点Next就行，后面可能还有几个界面，但应该是安装须知或者安装位置等，大家自行点击Next按键或者适合自己的位置就可以了，之后进入![选择 Typical 典型安装方式](mysql2.png)，这个如果没有特殊要求的话选择第一个Typical就可以了。![MySQL 程序安装完成，勾选运行配置工具](mysql4.png)界面不需要怎么操作，直接点击“Finish”就完成了。之后会出现以下界面![MySQL 配置向导欢迎页面](mysql5.png)，点击Next，![配置 MySQL 服务器类型、连接端口和防火墙选项](mysql6.png)，如果没有特殊需求，只要取消勾选Open Windows Firewall ports for network access就可以![设置 MySQL root 管理员密码](mysql7.png)，![配置 MySQL Windows 服务与开机自动启动](mysql8.png)点击Next，![设置 MySQL 数据目录的文件访问权限](mysql9.png)点击Next，![选择是否安装示例数据库](mysql10.png)点击Next，![检查即将应用的 MySQL 配置项目](mysql11.png)点击Next,![执行 MySQL 配置并查看各步骤的完成状态](mysql12.png)点击Execute,稍等一会，等所有选项的圆圈内都成为绿色小对勾之后就能点击Next了。![MySQL 配置完成](mysql13.png)点击Finish就可以了。

## 四、安装并激活 Navicat

下载完毕后，你可以直接安装。首先会出现一个安装须知，这个必须选同意，否则无法继续进行。后面安装位置选择一个合适的位置就行。创建桌面快捷操作创建或者不创建都可以。安装基本就结束了。
激活Navicat的话就直接点击桌面上的快捷方式，因为免费试用好像只能用2周左右，所以打开后会有一个界面询问是否购买长期产品或者是登录前面认证过的学术伙伴计划，这个登录的ID就是之前邮件里面写好的，直接粘贴过来就行，密码就是之前Navicat账号注册用过的密码。成功登录进去后是以下这个界面![登录激活后显示的 Navicat 界面](navicat_main.png),会出现非商业用途的说明和一些个性化选择![Navicat 首次启动设置页面（一）](navicat1.png),![Navicat 首次启动设置页面（二）](navicat2.png),![Navicat 首次启动设置页面（三）](navicat3.png),![Navicat 首次启动设置页面（四）](navicat4.png)。

## 五、使用 Navicat 连接 MySQL

点击桌面的Navicat图表，点击左上角的连接（“文件”的下方）![在 Navicat 中创建 MySQL 连接](connect1.png)，双击MySQL，![填写 MySQL 连接名称、主机、端口和账号密码](connect2.png)连接名称可以自己写，密码就是MySQL安装时配置的密码，剩下选项可以不修改。填写完毕后点解左下角“测试连接”选项，![Navicat 测试 MySQL 连接成功](connect3.png)出现该界面未连接成功，点击“确定”就完成连接了。

## 六、执行 SQL 验证安装结果

双击“我的连接”选项下刚刚取好连接名称的选项，出现以下界面![打开 MySQL 连接并进入查询界面](connect4.png)，可以点击“新建查询”，输入SQL语句：
'''sql
-- 创建一个练习数据库
CREATE DATABASE IF NOT EXISTS sql_practice
CHARACTER SET utf8mb4;

-- 接下来的操作都在这个数据库里进行
USE sql_practice;

-- 创建一张学生表
CREATE TABLE student (
    id INT PRIMARY KEY,
    name CHAR(50),
    age INT
);

-- 添加两条学生记录
INSERT INTO student (id, name, age)
VALUES
    (1, '张三', 20),
    (2, '李四', 21);

-- 查看学生表中的全部数据
SELECT * FROM student;
'''
点击运行，查看运行结果![执行 SQL，查看学生表的查询结果](test.png) 
