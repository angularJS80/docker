FROM centos:centos7


# 사용자 지정

USER root



# 언어셋 설치

RUN yum clean all \

 && yum repolist \

 && yum -y update \

 && sed -i "s/en_US/all/" /etc/yum.conf  \

 && yum -y reinstall glibc-common \

 && yum provides ifconfig \

 && yum provides netstat \

 && yum -y install wget \

 && yum -y install epel-release



# 기본설치

RUN  yum -y install net-tools wget tar unzip vi vim telnet net-tools curl openssl

# NodeJs
RUN yum -y install npm

# Git
Run yum -y install git
RUN git clone https://github.com/angularJS80/ng-try.git /usr/local/bin/ng-try
RUN npm install -g @angular/cli@latest
RUN npm install --prefix /usr/local/bin/ng-try
RUN npm install -g @angular/cli@8.0.0 
RUN ng build --prod
# 먼지몰라

RUN (cd /lib/systemd/system/sysinit.target.wants/; for i in *; do [ $i == \

systemd-tmpfiles-setup.service ] || rm -f $i; done); \

rm -f /lib/systemd/system/multi-user.target.wants/*;\

rm -f /etc/systemd/system/*.wants/*;\

rm -f /lib/systemd/system/local-fs.target.wants/*; \

rm -f /lib/systemd/system/sockets.target.wants/*udev*; \

rm -f /lib/systemd/system/sockets.target.wants/*initctl*; \

rm -f /lib/systemd/system/basic.target.wants/*;\

rm -f /lib/systemd/system/anaconda.target.wants/*;

#컨테이너 실행시 실행될 명령

CMD ["/usr/sbin/init"]
CMD ["/bin/bash"]
WORKDIR /usr/local/bin/nd-try
CMD ["pm2 start app.js"]
