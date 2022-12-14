### Mac install
https://realapril.tistory.com/18

### GRUB 기본부팅
https://ghostweb.tistory.com/826

### yum 에러
https://bono915.tistory.com/entry/Linux-%EB%A6%AC%EB%88%85%EC%8A%A4-yum-%EC%98%A4%EB%A5%98-Another-app-is-currently-holding-the-yum-lock-waiting-for-it-to-exit

### telnet
systemctl restart telnet.socket  
https://itdev4u.tistory.com/entry/CentOS-Telnet-%EC%84%A4%EC%B9%98

### 로그인 시 경고문
issue, issue.net	/etc/issue

### cd .. 차단
http://bywoong.com/post/1771

### 홈이탈방지
아래 디렉토리들의 권한을 변경하여 다른 폴더로의 접근 막음  
chmod -R  
/usr/local  
/boot  
/mnt  
/opt  
/bin  
/var

### 관리자 계정 root권한 주기
https://itgameworld.tistory.com/75

### Default 시작이 root
https://tother.tistory.com/151

### VNC
systemctl start vncserver@:1.service  
https://blog.naver.com/haengro/220346527168

https://lemontia.tistory.com/734

### vsftpd(ftp)
systemctl restart vsftpd.service  
https://goddaehee.tistory.com/73  
https://ckbcorp.tistory.com/1202  
\+ chroot_local_user=YES 활성화

### vsftpd "Failed to start Vsftpd ftp daemon" 에러
https://ckbcorp.tistory.com/1202

### proftpd(ftp)
시작 :	/usr/local/proftpd/sbin/proftpd  
종료 :	ps -ef | grep proftpd  
 &nbsp; kill -9 UID  
ftp user 확인  
ps aux | grep vsftpd  
vsftpd 깔려있으면 삭제해야함
https://blog.naver.com/PostView.nhn?blogId=anysecure3&logNo=221583997926

### crond.service(backup)
https://ansan-survivor.tistory.com/430

### ssh
systemctl restart sshd.service  
https://itdev4u.tistory.com/entry/CentOS-SSH-%EC%84%A4%EC%B9%98  
ssh [계정]@[ip]

### ssh 포트 변경 후 에러
https://zzokma.tistory.com/1517

### ssh Hot key 에러
https://m.blog.naver.com/midovan1/220250544307

### ssh 접속 메시지
https://www.withover.com/2012/06/ssh.html

###  C언어 컴파일
https://corock.tistory.com/240

### NFS 서버 구축
https://ansan-survivor.tistory.com/687

### exportfs: /etc/exports:1: syntax error: bad option list 에러 
https://ubuntuforums.org/showthread.php?t=1663927

### nginx 서버 구축
https://sepiros.tistory.com/25

### APM 구축
https://nyyang.tistory.com/25

### postgreSQL & DBeaver
systemctl start postgresql  
https://gsk121.tistory.com/392  
https://medium.com/@jinseok.choi/centos-7%EC%97%90%EC%84%9C-postgresql-11-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0-77bc0da9d0af  
https://meyouus.tistory.com/243  
https://zipeya.tistory.com/entry/postgresql-DB%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%A0%91%EC%86%8D-%EC%8B%9C-Peer-authentication%EC%97%90%EB%9F%AC-%EB%B0%9C%EC%83%9D-%EC%8B%9C-%ED%95%B4%EC%95%BC%ED%95%A0-%EA%B2%83  
https://nirsa.tistory.com/257  

### psql 명령어
https://dbrang.tistory.com/749

### APM 참고
https://www.manualfactory.net/10101  
https://zetawiki.com/wiki/CentOS_APM_%EC%84%A4%EC%B9%98_(yum)  

### php (사용할 기능들을 미리 고려해서 버전을 정해야 함. 기본 : 5.4)
yum install -y php*  
https://www.opentutorials.org/module/1701/10235  

### MariaDB
yum install -y mariadb*  
https://jeongyd.tistory.com/54  
https://bamdule.tistory.com/59  

### MySQL utf-8
https://zetawiki.com/wiki/MySQL_%EC%BA%90%EB%A6%AD%ED%84%B0%EC%85%8B_utf8_%EC%84%A4%EC%A0%95

### mariadb dbeaver utf-8
https://mitny.tistory.com/208

### DB 작업
https://bebhionn.tistory.com/8?category=239054  
https://m.blog.naver.com/bgpoilkj/220751401209

### php + mariadb 한글 깨짐
https://jhrun.tistory.com/140

### php reference
https://www.w3schools.com/php/func_mysqli_fetch_array.asp

### 채팅서버(irssi, unrealircd)
https://marcolenzo.eu/2016/01/30/install-unrealircd-server-on-centos-7/  
https://lovename.org/entry/irc-%EC%84%9C%EB%B2%84%EA%B5%AC%EC%B6%95  
https://operatingsystems.tistory.com/entry/Vul-IRC-%EC%84%9C%EB%B2%84-%EA%B5%AC%EC%B6%95  
unrealircd 설치된 경로로 이동  
./unrealircd start stop  

### 채팅클라이언트
yum -y install irssi  

### 채팅&음성 서버(teamspeak3)
https://tuxinit.com/how-to-install-teamspeak-server-on-centos-7-8/

### 방화벽 firewalld
http://help.nanuminet.com/bbs/board.php?bo_table=manual&wr_id=281  
https://m.blog.naver.com/tequini/220981170535

### SAMBA
yum -y install samba  
smbpasswd -a root  
vi /etc/samba/smb.conf  
```sh
[root]
        comment = "코멘트"
        path = /root  # 경로
        valid users = root <user> # 접근 가능한 유저
        read only = no  # 읽기 전용
        writable = yes  # 쓰기 가능
        public = no
        browseable =yes
        printable = no
        create mask = 0750
```
firewall-cmd --permanent --zone=public --add-service=samba  
firewall-cmd --reload  
systemctl enable smb	systemctl start smb

### SAMBA selinux
https://m.blog.naver.com/PostView.naver?blogId=hdlee91&logNo=150063056693&proxyReferer=https:%2F%2Fwww.google.com%2F

### SAMBA CentOS7
https://jjeongil.tistory.com/1519

### 로그서버
https://www.manualfactory.net/12970  

### 무료 도메인
https://hoing.io/archives/2279

### DNS bind
https://it-serial.tistory.com/13  
https://it-serial.tistory.com/14?category=958591

### sendmail
https://m.blog.naver.com/PostView.naver?blogId=picablue6252&logNo=221502528457&proxyReferer=https:%2F%2Fwww.google.com%2F
=> 메일 테스트는 # mail 이메일

### encoding
https://kkeuing.tistory.com/18

### WARNING: Group writable directory / 에러 해결
https://www.linuxquestions.org/questions/linux-server-73/sendmail-bi-problem-group-writable-712801/

### rsync mirror
https://blog.daum.net/boo-t/11397665  
https://lifegoesonme.tistory.com/373  
https://nota.tistory.com/77  
https://banitos.tistory.com/1

### 커널 업그레이드
https://nirsa.tistory.com/64

### LNAV 로그파일 분석
https://ko.linux-console.net/?p=2115

### DB 생성
https://brandon-dev.tistory.com/24

### MariaDB Error-Log 쌓기
https://bamdule.tistory.com/71

### 로그관리
https://power-girl0-0.tistory.com/164

### jar 배포
https://dev-coco.tistory.com/68

### Spring Boot Project 백그라운드 배포
https://whispertome.tistory.com/3

### quota
https://ansan-survivor.tistory.com/517

### quota xfs -> ext4
https://this1.tistory.com/entry/centos7-%ED%8C%8C%ED%8B%B0%EC%85%98-%ED%8C%8C%EC%9D%BC%EC%8B%9C%EC%8A%A4%ED%85%9C-%EB%B3%80%EA%B2%BD

### Nmap 사용법
https://snowyan23.tistory.com/6
https://hj-kwon.tistory.com/29

### Oracle DB
https://xxsiyoung.tistory.com/3

### 정보
insert into hs(num, name, k_name, pw, email, create_time)
values(1, 'slider', '전승진', 'wjsansrk', 'slider@jj.ac.kr', CURRENT_TIMESTAMP),
(2, 'sounder', '이세희', 'wjsansrk', 'sounder@jj.ac.kr', CURRENT_TIMESTAMP),
(3, 'tomber', '신승민', 'wjsansrk', 'tomber@jj.ac.kr', CURRENT_TIMESTAMP),
(4, 'none', '김민정', 'wjsansrk', 'none@jj.ac.kr', CURRENT_TIMESTAMP),
(5, 'khan', '진의정', 'wjsansrk', 'khan@jj.ac.kr', CURRENT_TIMESTAMP),
(6, 'none2', '배진석', 'wjsansrk', 'none2@jj.ac.kr', CURRENT_TIMESTAMP),
(7, 'anthony', '권오서', 'wjsansrk', 'anthony@jj.ac.kr', CURRENT_TIMESTAMP),
(8, 'reeker', '최아영', 'wjsansrk', 'reeker@jj.ac.kr', CURRENT_TIMESTAMP),
(9, 'eigher', '이기정', 'wjsansrk', 'eigher@jj.ac.kr', CURRENT_TIMESTAMP),
(10, 'daver', '이승태', 'wjsansrk', 'daver@jj.ac.kr', CURRENT_TIMESTAMP);

insert into hs(num, name, k_name, pw, email, create_time)
values(1, 'slider', '전승진', 'wjsansrk', 'slider@jj.ac.kr', now()),
(2, 'sounder', '이세희', 'wjsansrk', 'sounder@jj.ac.kr', now()),
(3, 'tomber', '신승민', 'wjsansrk', 'tomber@jj.ac.kr', now()),
(4, 'none', '김민정', 'wjsansrk', 'none@jj.ac.kr', now()),
(5, 'khan', '진의정', 'wjsansrk', 'khan@jj.ac.kr', now()),
(6, 'none2', '배진석', 'wjsansrk', 'none2@jj.ac.kr', now()),
(7, 'anthony', '권오서', 'wjsansrk', 'anthony@jj.ac.kr', now()),
(8, 'reeker', '최아영', 'wjsansrk', 'reeker@jj.ac.kr', now()),
(9, 'eigher', '이기정', 'wjsansrk', 'eigher@jj.ac.kr', now()),
(10, 'daver', '이승태', 'wjsansrk', 'daver@jj.ac.kr', now());

### Cubrid
https://zetawiki.com/wiki/CentOS7_%ED%81%90%EB%B8%8C%EB%A6%AC%EB%93%9C_%EC%84%A4%EC%B9%98

### mssql
https://ansan-survivor.tistory.com/1202
