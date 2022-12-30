## day5

1byte = 2^8 = 256
2byte = 2^16 = 65536
4byte = 2^32 = 42.9억
8byte = 2^64 = 1경

ip v4 = 2^32
ip v6 = 2^128

사설ip
공인ip

DHCP == 유동IP : 접속할때마다 IP 주소 변경됨
SERVER = 서버, 관리, 유지비 돈이 많이든다~
SO! 서버를 빌려서 쓴다 : 호스팅

<ip>

ip addr
g.w
netmask
dns

root@sean:~# nmap localhost

중요 포트 번호
root@sean:~# grep http /etc/services

80 http
21 ftp
25 smtp
143 imap
110 pop3
53 domain

root@sean:~# nl /etc/resolv.conf


넷마스크!!
