#------------------------- GIT ��Ŀ���� v1.1 -------------------------#
0x01 ���ɲ��ϴ�SSH RSA��Կ�ļ�id_rsa.pub�ύ��Administrator 
----------------------------------------------------
��Ҫ�����л���(unix/linux/mac/cygwin/mingw)
���ɷ�����ʹ��ssh-keygen/PuTTYgen����Ҫ��������
��~/.ssh/id_rsa.pub�����������͸� BENM <binxiaofeng@gmail.com>

0x02 ��װGit��Python���������
----------------------------------------------------
git����: http://git-scm.com/
��ʼ����git
git config --global user.name "Your Name"
git config --global user.email "Your Email"
����python�������pip��easy_install��װ
Crypto (>=2.6)
rsa (>=3.1.4)
python-gnupg (>=0.3.7)

0x03 ������Ŀ����Ȩ�޺�branch����
----------------------------------------------------
�ύproject��
�ύbranchȨ��

0x04 ��ù����ύ��������ez_git.pyo 
----------------------------------------------------
���ǰ�����������Administrator�������GitHub����
GitHub���ص�ַ��https://github.com/BENMFeng/ez_git
Ϊ��֤�ʻ�����Ŀ��ȫ�����˼��ܱ��봦����Ҫ��Administrator����gpg��Կlicense
����.gpglicĿ¼�ŵ�ez_git.pyoͬһ���ļ�����
�ó�����Ҫ�����¹��ܣ�
(1) ��ȡIP��Ȩ�ޡ���֧�������ã�
(2) ����master��branch��
(3) �ύ����

0x05 �޸ı��ع��̣�����ez_git���ϴ�����
----------------------------------------------------
1. ���ñ���git�ֿ�(git config/git init����ɲ���ʼ������ez_gitʹ��0��)
2. git checkout branch����Ȩ�����ڵ�branch��
3. ���ع���Ŀ¼�޸Ĺ���;
4. �ϴ������ع���GIT�ݴ�����;����ѡ��
5. git commit/git tag(��ѡ��
6. ez_git����ʹ�÷���
	Usage Example: �÷��� python ez_git.pyo --help
	0) ������ʼ���� 
	��~/.bashrc��~/.bash_profile�򻷾�����������
	export EZ_GIT=/path/ez_git    #/path/ez_gitΪez_git.pyo������Ĵ��·��
	python $EZ_GIT/ez_git.pyo -p **yourprojectname -b **yourbranch -u
	'''�����Խ��ļ��У���ĿĿ¼���Զ�ͬ������ǰĿ¼'''
	1) ֱ���ύ���̣�python $EZ_GIT/ez_git.pyo -p **yourprojectname -b **yourbranch
	2) ˳���ύע�ͣ�python $EZ_GIT/ez_git.pyo -p **yourprojectname -b **yourbranch -m '**updatemessage'
	3) �ȸ������branch���ϴ����룺python $EZ_GIT/ez_git.pyo -p **yourprojectname -b **yourbranch --syn
	4) �ϴ������ͬ��һ��master branch: python $EZ_GIT/ez_git.pyo -p **yourprojectname -b **yourbranch --update
	'''
	**yourprojectname ��ָ����Ҫͬ�����ص�project��
	**yourbranch      ��ָ��project����ӵ�еķ�֧
	**updatemessage   ���ύʱ��Ҫע�͵�����

BENM FENG <binxiaofeng@gmail.com>
BD: 2014-12-25
Modified: 2015-04-30
-------------------------------------------------------------------------