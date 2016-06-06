
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
- Virtualbox���� �Ʒ� ��ɾ� �տ� sudo �� ����


- �ڹ�, ��Ŭ����, git, wget ��ġ�ϱ�
```
apt-get update -y
apt-get install wget git openjdk-7-jdk  eclipse  -y
```

- Maven ��ġ( ������ ���� �� ���嵵�� )
```
cd ~/
wget  https://archive.apache.org/dist/maven/maven-3/3.2.5/binaries/apache-maven-3.2.5-bin.tar.gz
tar xvf apache-maven-3.2.5-bin.tar.gz

cat <<EOT >> ~/.bashrc
JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64
MAVEN_HOME=`echo $HOME`/apache-maven-3.2.5

export PATH=\$JAVA_HOME/bin:\$MAVEN_HOME/bin:\$PATH
EOT

source ~/.bashrc
```

- ��Ŭ���� �ֽŹ��� ��ġ
- ������ �������� ��ġ����. maven ��Ŭ���� �÷����� ��ġ�ÿ� ���� ���� ��쿡�� ��ġ��.
```

cd ~/
wget http://dist.springsource.com/release/STS/3.6.4.RELEASE/dist/e4.4/groovy-grails-tool-suite-3.6.4.RELEASE-e4.4.2-linux-gtk-x86_64.tar.gz
tar xvf groovy-grails-tool-suite-3.6.4.RELEASE-e4.4.2-linux-gtk-x86_64.tar.gz

```



- �����ҽ� �ޱ�
```
cd ~/

git clone https://github.com/mahmoudparsian/data-algorithms-book/
```

## ��Ŭ���� ����
- ������� �޴��� Eclipse�� ��ϵǾ� ����.
- �޴��� ���ؼ� ��Ŭ���� ����
- Welcome ���� ������ ��Ȳ���� ����,  Welcome�ǿ� �ִ� x ��ư�� Ŭ����.
### maven ��Ŭ���� �÷������� ��ġ�ϱ�
    - ��Ŭ���� -> ��ܸ޴��� -> Help -> Install New Software ... 
	- Work width �Էº��忡 Indigo Update Site ��� �Է��ϰ�, ������.
	- Work width �Էº��� �Ʒ��� ���� ���� ����� ������, ���⼭ collaboration�� ����.
	- collaboration���� ���� ���� ��Ű���� �ְ�,  m2e-Maven Integration for Eclipse�� üũ�� �Ŀ� Next��ư Ŭ��
	- ���� ȭ�鿡�� �ٽ� Next ��ư Ŭ��
	- ���� ȭ�鿡�� ���̼��� ���Ǹ� �����ϰ� Finish ��ư Ŭ��
	- ��Ŭ���� restart�ϴ� �˸�â�� ������, Yes Ŭ��

### �ϵ� MapReduce �ǽ��� Maven ������Ʈ ����
- ��Ŭ���� -> ��ܸ޴��� -> File -> Project...
- New Project ���ڵ�â���� Maven -> Maven Project �� �����ϰ� Next ��ư Ŭ����
- ����ȭ�鿡��  �׳� Next ��ư Ŭ����
- ����ȭ�鿡�� maven-archetype-quickstart �� ���õǾ� �ְ�, �׳� Next ��ư Ŭ����
- ����ȭ�鿡�� 
    - Goup id �Է��ʵ忡  org.biospin.bigbio   ��� �Է�
    - Arifact id �Է��ʵ忡 hadoop1x  ��� �Է��ϰ� Next ��ư Ŭ����.
- ����ȭ�鿡���� ������Ʈ�� ������� ȭ���� ����.
![](eclipse_01.png)

- pom.xml ����
    - pom.xml ����Ŭ���ϰ�, ����â�� �Ʒ��� Overview ������ �����Ȱ���  pom.xml ���� �����ϸ� �ؽ�Ʈ���� ������.
	- dependency�� �߰���.
```
dependency

<dependency>
    <groupId>org.apache.hadoop</groupId>
    <artifactId>hadoop-core</artifactId>
    <version>1.2.0</version>
</dependency>


```
	



