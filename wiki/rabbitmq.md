### erlang
```
wget https://packages.erlang-solutions.com/erlang-solutions-1.0-1.noarch.rpm
sudo rpm -Uvh erlang-solutions-1.0-1.noarch.rpm

sudo rpm --import https://packages.erlang-solutions.com/rpm/erlang_solutions.asc

sudo vi /etc/yum.repos.d/erlang_solutions.repo

[erlang-solutions]
name=Centos $releasever - $basearch - Erlang Solutions
baseurl=https://packages.erlang-solutions.com/rpm/centos/$releasever/$basearch
gpgcheck=1
gpgkey=https://packages.erlang-solutions.com/rpm/erlang_solutions.asc
enabled=1

sudo yum install erlang --enablerepo=erlang-solutions
```