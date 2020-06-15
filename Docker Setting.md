# Docker Study Part 1 - Docker setting

## 1. Version info
- CentOS
<pre>
[dptest@localhost ~]$ cat /etc/redhat-release
CentOS Linux release 7.8.2003 (Core)
</pre>

- Linux
<pre>
[dptest@localhost ~]$ uname -a
Linux localhost.localdomain 3.10.0-1127.el7.x86_64 #1 SMP Tue Mar 31 23:36:51 UTC 2020 x86_64 x86_64 x86_64
</pre>

- Docker
<pre>
[dptest@localhost ~]$ docker -v
Docker version 1.13.1, build 64e9980/1.13.1
</pre><br>

## 2. How to install Docker
### A.(Option) Provide super user(sudo) authority to my user
<pre>
[dptest@localhost ~]$ su - root
Password: 
[root@localhost ~]# vi /etc/sudoers
</pre>
&nbsp;Put "dptest ALL=(ALL)  ALL" statement at the bottom of the file.
<pre>
...
## Read drop-in files from /etc/sudoers.d (the # here does not mean a comment)
#includedir /etc/sudoers.d
dptest ALL=(ALL)  ALL
</pre>

### B. Install Docker through "yum" command.
<pre>
[dptest@localhost ~]# sudo yum install docker
[dptest@localhost ~]# sudo chmod 666 /var/run/docker.sock
</pre>
