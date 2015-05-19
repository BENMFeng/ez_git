GIT 加密信道项目管理 v1.1
=============
0x01 生成并上传SSH RSA公钥文件id_rsa.pub提交给Administrator 
----------------------------------------------------
需要命令行环境(unix/linux/mac/cygwin/mingw)
生成方法，使用ssh-keygen/PuTTYgen，不要设置密码
把~/.ssh/id_rsa.pub拷贝出来发送给 Administrator

0x02 安装Git和Python，及需求包
----------------------------------------------------
git下载: http://git-scm.com/

初始设置git:

<code>git config --global user.name "Your Name"</code>

<code>git config --global user.email "Your Email"</code>

以下python库可以用pip或easy_install安装

Crypto (>=2.6)

rsa (>=3.1.4)

python-gnupg (>=0.3.7)

0x03 申请项目管理权限和branch配置
----------------------------------------------------
提交project名

提交branch权限

0x04 获得工程提交辅助程序ez_git.pyo 
----------------------------------------------------
完成前三个步骤后向Administrator申请或在GitHub下载

GitHub下载地址：https://github.com/BENMFeng/ez_git

为保证帐户和项目安全，作了加密编译处理，需要向Administrator申请gpg密钥license，
并将.gpglic目录放到ez_git.pyo同一个文件夹中，
该程序主要含以下功能：

(1) 获取IP及权限、分支管理配置；

(2) 更新master及branch；

(3) 提交工程

0x05 修改本地工程，并用ez_git来上传代码
----------------------------------------------------
1. 配置本地git仓库(git config/git init，亦可不初始化，见ez_git使用0）)

2. git checkout branch（你权限所在的branch）

3. 本地工作目录修改工程;

4. 上传至本地工作GIT暂存区域;（可选）

5. git commit/git tag(可选）

6. ez_git程序使用方法

Usage Example: 用法见 python ez_git.pyo --help

*   初级初始化： 

在~/.bashrc或~/.bash_profile或环境变量中声明(#/path/ez_git为ez_git.pyo主程序的存放路径)：
		
<code>export EZ_GIT=/path/ez_git</code>   

运行
		
<code>python $EZ_GIT/ez_git.pyo -p **yourprojectnam**e -b **yourbranch** -u</code>
	
_**不用自建文件夹，项目目录会自动同步到当前目录**_
		
*   直接提交工程：
	
<code>python $EZ_GIT/ez_git.pyo -p **yourprojectname** -b **yourbranch**</code>
	
*   顺带提交注释：
	
<code>python $EZ_GIT/ez_git.pyo -p **yourprojectname** -b **yourbranch** -m '**updatemessage**'</code>
	
*   先更新你的branch再上传代码：
	
<code>python $EZ_GIT/ez_git.pyo -p **yourprojectname** -b **yourbranch** --update</code>
	
*   上传代码后同步一下完整master分支(必须具备master分支权限）: 
	
<code>python $EZ_GIT/ez_git.pyo -p **yourprojectname** -b **yourbranch** --sync</code>
	
**yourprojectname** 是指你需要同步本地的project名

**yourbranch**      是指该project你所拥有的分支

**updatemessage**   是提交时需要注释的文字

---
BENM FENG

BD: 2014-12-25

Modified: 2015-05-01
