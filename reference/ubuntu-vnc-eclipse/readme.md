
# ��������� �ϵ� mapreduce ����ȯ�� �����


## Docker�� VNC�� ��Ŭ���� ��ġ

- ����) ��� ȯ���� �����ϰ� ��Ŀ�� commit�Ҷ� ������ ��� �߻��ؼ� ������ �� ���ư���. 
- ����) �׳� virtualbox���� ��������� �ϴ°��� ������ ����.
- ����) ���ڿ�~~  ��ð��� ������ �����ϰ� �Ʒ��� ���� �غ���..
- ����) ���� ������ �� �ǰ���..~~~



- https://hub.docker.com/r/kaixhin/vnc/  �̰��� �̿���.
- kaixhin/vnc  Docker �̹��� ��ġ �� ����
- VNC�� ����Ʈ �н������ password,  ���浵 ������.
```
docker pull kaixhin/vnc
docker run -d -p 5901:5901 kaixhin/vnc
```

- TightVNC Ŭ���̾�Ʈ ��ġ 
```
http://www.tightvnc.com/download/2.7.10/tightvnc-2.7.10-setup-64bit.msi
```

- TightVNC ������ ��ġ���� ���� Ŭ���̾�Ʈ�� ��ġ�Ŀ� ����
- remote server : 192.168.xxx.xxx:5901

## VNC�� Docker ���η� �����ؼ� �����ϱ�
- virtualbox�� ����������� �̿� �����ϰ� ������.


- �ڹ�, ��Ŭ����, git, wget ��ġ�ϱ�
```
apt-get install wget git openjdk-7-jdk  eclipse  -y
```

- Maven ��ġ( ������ ���� �� ���嵵�� )
```
cd ~/
wget  https://archive.apache.org/dist/maven/maven-3/3.2.5/binaries/apache-maven-3.2.5-bin.tar.gz
tar xvf apache-maven-3.2.5-bin.tar.gz

cat <<EOT >> ~/.bashrc
JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64
MAVEN_HOME=/root/apache-maven-3.2.5

export PATH=$JAVA_HOME/bin:$MAVEN_HOME/bin:$PATH
EOT

source ~/.bashrc
```

- �����ҽ� �ޱ�
```
cd ~/

git clone https://github.com/mahmoudparsian/data-algorithms-book/
```
