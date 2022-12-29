## day3
  1. 
## day4 : ubuntu 설치 후 설정


sudo -i

sudo passwd

su -


whoam i : root


script Linux-Set
date
timezon 변경!!

timedatectl set-timezone Asia/Seoul
date

<파일에 넣기>
vi ~/.bash_aliases
alias ai='apt -y install'
alias h='history'
alias c='clear'
alias lh = 'ls -Alh'
. ~/.profile -> 재부팅과 똑같은 효과!!즉, alias 적용

vi ~/.vimrc
se nu ai ci si ts=4 sw=4 ruler title showmatch
syntax on
hi comment ctermfg=red

ai ncal
locale
nl /etc/default/locale
vi /etc/default/locale

#~~
LANG=ko_KR.UTF-8
ai language-pack-ko
update-locale LANG=ko_KR.UTF-8
새창 : locale

<duplicate>:
su -

apt -y installed gcc g++ default-jdk apache2 mysql-server tomcat9 sqlite sendmail mailutils tree lynx(textbrowser) glibc-doc mandoc rdate

cp .vimrc /etc/skel/ -> 사용자 만들때 디폴트값 설정

useradd -D
useradd -D -s /bin/bash 
useradd -D

vi /etc/login.defs
CREATE_HOME yes

useradd ace
passwd ace

df -h : 파티션 정보

ai quota

<duplicate>

su -

groupadd NC
useradd -G NC nc1
useradd -G NC nc2
useradd -G NC nc3
useradd -G NC nc4
useradd -G NC nc5
passwd nc1
passwd nc2
passwd nc3
passwd nc4
passwd nc5

nl etc/group
<<데이터베이스 설정!!!!!!!!!>>
mysql : default는 패스워드가 없고 루트관리자이다 
select user();
-> 설정을 해주자!!!
use mysql
alter user 'root'@'localhost' identified by 'jj'; -> 루트 패스워드 설정
create user myace@localhost identified by '1'; -> 사용자 만듬 id : myace pw:1
grant all privileges on acedb.* to myace@localhost; -> acedb의 모든 권한 허용 myace에게
flush privileges;

끝!!

test->
ace로 로그인
pw 1

mysql -u myace -p
pw : 1

select user();
show databases;
create database acedb;
use acedb;
create table A(su int);
insert into A values(40);
select * A;

-> root 계정
mysql -u root -p
jj


mysql -u 'root'@'localhost' -p(error) 

<<웹서비스 설정>>

service apache2 start
cd /var/www/html
ls -> index.html
mv index.html old.html
vi index.html
~~~~ html 문서 작성

<<quota>>

quota -> no mesg!!!
vi /etc/fstab -> /home에 ,usrquota 추가
mount -o remount /home
quotaon -avug
quotaoff -avug
quotacheck -avugm
quotaon -avug
ls /home/
repquota -a

edquota -t : 건드리지 않고 컨트롤 x
edquota -u nc1    : soft:5000 hard:6000
repquota-a
edquota -p nc1 nc2 nc3

login : nc1 , nc5 확인해보기!!!
확인법:
quota
cp -r /etc .
du -sh ~

poweroff
