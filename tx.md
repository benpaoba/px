What are you dong?

cd E:/  ����Ŀ¼

ls ��ʾ�ļ���Ŀ¼���൱�ڲ鿴��  [ ls -al ] �鿴��ǰĿ¼�µ������ļ����������ص�

mkdir  ����Ŀ¼

touch �����ļ�-

echo Hello > README.md   �����ļ� README.md ����Ϊ Hello


pwd ��ʾ��ǰ·��

clear ����

cat �鿴�ļ�����

git init  ��ָ��Ŀ¼�´��� .git ������Ϊ���ǲֿ�

git status ��ȡ��ǰ����Ŀ¼��״̬����Щ����ӵģ���Щ���޸ĵ�

git add xxx.md  ���ļ���ӵ��ֿ�

git commit �ύ���ѻ����������ݣ��ύ���ֿ��ڲ������ݿ⣬�޸ĵ���ʷ
����ת��ҳ�� ���� a ���Խ��б༭  �� �� Esc ��  �ٰ� shift + :  ���� wq �˳���

git commit -am "�ύʱ��ǵ�����"   ����ֱ���ύ�ˣ�����Ҫ��תҳ�棩�� -a �����ύ�����е��޸ģ� - m ��������ύ����־��


git log �鿴�ύ����־

git log xxx.md  �鿴���ļ�ÿ�ε��ύ��¼

git log --help �鿴��ϸ����־

git  --help �鿴 git ����Щָ��

gitk ���е��ύ����ʾ������

git gui UI���ڲ���



git Զ�̷���
1.����Ӧ��
2�� �ڴ�����Ӧ������ӹ�Կ���� ��Կ������ ���� git Bush ������ ���� git gui ���� UI ���ڣ�������Ͻǵ� help ��Ȼ�� SSE ��Կ�� 
3.���������� cd  ������ / .ssh/    ( ��Կ������  C:\Users\Administrator\.ssh)  
4.ls

5. git remote add origin git@git.oschina.net:www_wang/GitDemo.git �����ӣ�

6.git push -u origin master ���ύ��




Git��������
�鿴����ӡ��ύ��ɾ�����һأ������޸��ļ�

git help <command> # ��ʾcommand��help

git show # ��ʾĳ���ύ������ git show $id

git co -- <file> # �����������޸�

git co . # �����������޸�

git add <file> # �������ļ��޸��ύ�������ݴ���

git add . # �������޸Ĺ��Ĺ����ļ��ύ�ݴ���

git rm <file> # �Ӱ汾����ɾ���ļ�

git rm <file> --cached # �Ӱ汾����ɾ���ļ�������ɾ���ļ�

git reset <file> # ���ݴ����ָ��������ļ�

git reset -- . # ���ݴ����ָ��������ļ�

git reset --hard # �ָ����һ���ύ����״̬���������ϴ��ύ������б����޸�

git ci <file> git ci . git ci -a # ��git add, git rm��git ci�Ȳ������ϲ���һ����������������������������������������������������������������������������git ci -am "some comments"

git ci --amend # �޸����һ���ύ��¼

git revert <$id> # �ָ�ĳ���ύ��״̬���ָ���������Ҳ�������ύ����

git revert HEAD # �ָ����һ���ύ��״̬

�鿴�ļ�diff

git diff <file> # �Ƚϵ�ǰ�ļ����ݴ����ļ����� git diff

git diff <id1><id1><id2> # �Ƚ������ύ֮��Ĳ���

git diff <branch1>..<branch2> # ��������֧֮��Ƚ�

git diff --staged # �Ƚ��ݴ����Ͱ汾�����

git diff --cached # �Ƚ��ݴ����Ͱ汾�����

git diff --stat # �����Ƚ�ͳ����Ϣ

�鿴�ύ��¼

git log  <file> # �鿴���ļ�ÿ���ύ��¼

git log -p <file> # �鿴ÿ����ϸ�޸����ݵ�diff

git log -p -2 # �鿴���������ϸ�޸����ݵ�diff

git log --stat #�鿴�ύͳ����Ϣ

tig

Mac�Ͽ���ʹ��tig����diff��log��brew install tig

Git ���ط�֧����

�鿴���л���������ɾ����֧

git br -r # �鿴Զ�̷�֧

git br <new_branch> # �����µķ�֧

git br -v # �鿴������֧����ύ��Ϣ

git br --merged # �鿴�Ѿ����ϲ�����ǰ��֧�ķ�֧

git br --no-merged # �鿴��δ���ϲ�����ǰ��֧�ķ�֧

git co <branch> # �л���ĳ����֧

git co -b <new_branch> # �����µķ�֧�������л���ȥ

git co -b <new_branch> <branch> # ����branch�����µ�new_branch

git co $id # ��ĳ����ʷ�ύ��¼checkout���������޷�֧��Ϣ���л���������֧���Զ�ɾ��

git co $id -b <new_branch> # ��ĳ����ʷ�ύ��¼checkout������������һ����֧

git br -d <branch> # ɾ��ĳ����֧

git br -D <branch> # ǿ��ɾ��ĳ����֧ (δ���ϲ��ķ�֧��ɾ����ʱ����Ҫǿ��)

 ��֧�ϲ���rebase

git merge <branch> # ��branch��֧�ϲ�����ǰ��֧

git merge origin/master --no-ff # ��ҪFast-Foward�ϲ���������������merge�ύ

git rebase master <branch> # ��master rebase��branch���൱�ڣ� git co <branch> && git rebase master && git co master && git merge <branch>

 Git��������(�����ڶ�̨�����Ͽ���ͬ��ʱ��)

git diff > ../sync.patch # ���ɲ���

git apply ../sync.patch # �򲹶�

git apply --check ../sync.patch #���Բ����ܷ�ɹ�

 Git�ݴ����

git stash # �ݴ�

git stash list # ������stash

git stash apply # �ָ��ݴ������

git stash drop # ɾ���ݴ���

GitԶ�̷�֧����

git pull # ץȡԶ�ֿ̲����з�֧���²��ϲ�������

git pull --no-ff # ץȡԶ�ֿ̲����з�֧���²��ϲ������أ���Ҫ����ϲ�

git fetch origin # ץȡԶ�ֿ̲����

git merge origin/master # ��Զ������֧�ϲ������ص�ǰ��֧

git co --track origin/branch # ����ĳ��Զ�̷�֧������Ӧ�ı��ط�֧

git co -b <local_branch> origin/<remote_branch> # ����Զ�̷�֧�������ط�֧������ͬ��

git push # push���з�֧

git push origin master # ����������֧�Ƶ�Զ������֧

git push -u origin master # ����������֧�Ƶ�Զ��(����Զ������֧�򴴽������ڳ�ʼ��Զ�ֿ̲�)

git push origin <local_branch> # ����Զ�̷�֧�� origin��Զ�ֿ̲���

git push origin <local_branch>:<remote_branch> # ����Զ�̷�֧

git push origin :<remote_branch> #��ɾ�����ط�֧(git br -d <branch>)��Ȼ����pushɾ��Զ�̷�֧

GitԶ�ֿ̲����

GitHub

git remote -v # �鿴Զ�̷�������ַ�Ͳֿ�����

git remote show origin # �鿴Զ�̷������ֿ�״̬

git remote add origin git@ github:robbin/robbin_site.git # ���Զ�ֿ̲��ַ

git remote set-url origin git@ github.com:robbin/robbin_site.git # ����Զ�ֿ̲��ַ(�����޸�Զ�ֿ̲��ַ) git remote rm <repository> # ɾ��Զ�ֿ̲�

����Զ�ֿ̲�

git clone --bare robbin_site robbin_site.git # �ô��汾����Ŀ�������汾�ֿ�

scp -r my_project.git git@ git.csdn.net:~ # �����ֿ��ϴ�����������

mkdir robbin_site.git && cd robbin_site.git && git --bare init # �ڷ������������ֿ�

git remote add origin git@ github.com:robbin/robbin_site.git # ����Զ�ֿ̲��ַ

git push -u origin master # �ͻ����״��ύ

git push -u origin develop # �״ν�����develop��֧�ύ��Զ��develop��֧������track

git remote set-head origin master # ����Զ�ֿ̲��HEADָ��master��֧

Ҳ�����������ø���Զ�̿�ͱ��ؿ�

git branch --set-upstream master origin/master

git branch --set-upstream develop origin/develop






			Linux ����ָ��



ls����        ��ʾ�ļ���Ŀ¼

     -l           �г��ļ���ϸ��Ϣl(list)

     -a          �г���ǰĿ¼�������ļ���Ŀ¼���������ص�a(all)

mkdir         ����Ŀ¼

     -p           ����Ŀ¼�����޸�Ŀ¼���򴴽�p(parent)

cd               �л�Ŀ¼

touch          �������ļ�

echo            �����������ݵ��ļ���

cat              �鿴�ļ�����

cp                ����

mv               �ƶ���������

rm               ɾ���ļ�

     -r            �ݹ�ɾ������ɾ����Ŀ¼���ļ�

     -f            ǿ��ɾ��

find              ���ļ�ϵͳ������ĳ�ļ�

wc                ͳ���ı����������������ַ���

grep             ���ı��ļ��в���ĳ���ַ���

rmdir           ɾ����Ŀ¼

tree             ���νṹ��ʾĿ¼����Ҫ��װtree��

pwd              ��ʾ��ǰĿ¼

ln                  ���������ļ�

more��less  ��ҳ��ʾ�ı��ļ�����

head��tail    ��ʾ�ļ�ͷ��β����

ctrl+alt+F1  ������ȫ��ģʽ

 

ϵͳ��������

stat              ��ʾָ���ļ�����ϸ��Ϣ����ls����ϸ

who               ��ʾ���ߵ�½�û�

whoami          ��ʾ��ǰ�����û�

hostname      ��ʾ������

uname           ��ʾϵͳ��Ϣ

top                ��̬��ʾ��ǰ�ķ���Դ��������Ϣ

ps                  ��ʾ˲�����״̬ ps -aux

du                  �鿴Ŀ¼��С du -h /home���е�λ��ʾĿ¼��Ϣ

df                  �鿴���̴�С df -h ���е�λ��ʾ������Ϣ

ifconfig          �鿴�������

ping                ����������ͨ

netstat          ��ʾ����״̬��Ϣ

man                ��������ˣ�������  �磺man ls

clear              ����

alias               ������������ �磺alias showmeit="ps -aux" ��������ʹ��unaliax showmeit

kill                 ɱ�����̣���������ps �� top����鿴���̵�id��Ȼ������kill����ɱ�����̡�

 

���ѹ���������

gzip��

bzip2��

tar:                ���ѹ��

     -c              �鵵�ļ�

     -x              ѹ���ļ�

     -z              gzipѹ���ļ�

     -j              bzip2ѹ���ļ�

     -v              ��ʾѹ�����ѹ������ v(view)

     -f              ʹ�õ���

����

tar -cvf /home/abc.tar /home/abc              ֻ�������ѹ��

tar -zcvf /home/abc.tar.gz /home/abc        ���������gzipѹ��

tar -jcvf /home/abc.tar.bz2 /home/abc      ���������bzip2ѹ��

��Ȼ��������ѹ������ֱ���滻���������  tar -cvf  / tar -zcvf  / tar -jcvf �еġ�c�� ���ɡ�x�� �Ϳ����ˡ�

 

�ػ�/��������

shutdown

     -r             �ػ�����

     -h             �ػ�������

     now          ���̹ػ�

halt               �ػ�

reboot          ����

 

Linux�ܵ�

��һ������ı�׼�����Ϊ��һ������ı�׼���롣Ҳ���ǰѼ��������������ʹ�ã���һ���������ǰһ������Ľ����

����grep -r "close" /home/* | more       ��homeĿ¼�������ļ��в��ң�����close���ļ�������ҳ�����

 

Linux���������

dpkg (Debian Package)�����ߣ����������.deb��׺�����ַ����ʺ�ϵͳ��������������¡�

���簲װtree����İ�װ�����Ƚ�tree.deb����Linuxϵͳ�С���ʹ���������װ��

sudo dpkg -i tree_1.5.3-1_i386.deb         ��װ���

sudo dpkg -r tree                                     ж�����

 

ע����tree.deb����Linuxϵͳ�У��ж��ַ�ʽ��VMwareTool��ʹ�ù��ط�ʽ��ʹ��winSCP���ߵȣ�

APT��Advanced Packaging Tool���߼�������ߡ����ַ����ʺ�ϵͳ�ܹ����ӻ������������

��Ȼ��treeΪ��

sudo apt-get install tree                         ��װtree

sudo apt-get remove tree                       ж��tree

sudo apt-get update                                 �������

sudo apt-get upgrade        

 

��.rpm�ļ�תΪ.deb�ļ�

.rpmΪRedHatʹ�õ������ʽ����Ubuntu�²���ֱ��ʹ�ã�������Ҫת��һ�¡�

sudo alien abc.rpm

 

vimʹ��

vim����ģʽ������ģʽ������ģʽ���༭ģʽ��ʹ��ESC��i�����л�ģʽ��

����ģʽ�£�

:q                      �˳�

:q!                     ǿ���˳�

:wq                   ���沢�˳�

:set number     ��ʾ�к�

:set nonumber  �����к�

/apache            ���ĵ��в���apache ��n������һ����shift+n��һ��

yyp                   ���ƹ�������У���ճ��

h(����һ���ַ���)��j(��һ�С�)��k(��һ�С�)��l(����һ���ַ���)

 

�û����û������

/etc/passwd    �洢�û��˺�

/etc/group       �洢���˺�

/etc/shadow    �洢�û��˺ŵ�����

/etc/gshadow  �洢�û����˺ŵ�����

useradd �û���

userdel �û���

adduser �û���

groupadd ����

groupdel ����

passwd root     ��root��������

su root

su - root 

/etc/profile     ϵͳ��������

bash_profile     �û���������

.bashrc              �û���������

su user              �л��û������������ļ�.bashrc

su - user            �л��û������������ļ�/etc/profile ������bash_profile

�����ļ����û����û���

sudo chown [-R] owner[:group] {File|Directory}

���磺����jdk-7u21-linux-i586.tar.gzΪ���������û�hadoop����hadoop

Ҫ���л����ļ��������û����顣����ʹ�����

sudo chown root:root jdk-7u21-linux-i586.tar.gz

 

�ļ�Ȩ�޹���

���ֻ���Ȩ��

R           ��         ��ֵ��ʾΪ4

W          д         ��ֵ��ʾΪ2

X           ��ִ��  ��ֵ��ʾΪ1



��ͼ��ʾ��jdk-7u21-linux-i586.tar.gz�ļ���Ȩ��Ϊ-rw-rw-r--

-rw-rw-r--һ��ʮ���ַ����ֳ��ĶΡ�

��һ���ַ���-����ʾ��ͨ�ļ������λ�û����ܻ���֡�l�����ӣ���d����ʾĿ¼

�ڶ����ĸ��ַ���rw-����ʾ��ǰ�����û���Ȩ�ޡ�   ��������ֵ��ʾΪ4+2=6

�������߸��ַ���rw-����ʾ��ǰ�������Ȩ�ޡ�      ��������ֵ��ʾΪ4+2=6

�ڰ˾�ʮ���ַ���r--����ʾ�����û�Ȩ�ޡ�              ��������ֵ��ʾΪ2

���Բ������ļ���Ȩ������ֵ��ʾΪ662 