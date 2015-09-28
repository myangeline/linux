# ubuntu安装jdk

## 1.去ORACLE官网下载最新版的JDK，解压到指定目录即可，例如 /usr/local/java
## 2.添加到系统环境变量 
使用gedit打开 /etc/profile文件
    
    >$ sudo gedit /etc/profile

在编辑器中添加如下代码:
    
    export JAVA_HOME=/usr/local/java/jdk1.8.0_40
    export JRE_HOME=$JAVA_HOME/jre
    export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib/rt.jar
    export PATH=$PATH:$JAVA_HOME/bin

## 3.设置默认运行时环境,也就是jre(需要根据实际情况来设定,由于我安装的是完整的jdk,里面自带的jre)
	
	>$ sudo update-alternatives --install "/usr/bin/java" "java" "/usr/local/java/jdk1.8.0_40/jre/bin/java" 1
	>$ sudo update-alternatives --install "/usr/bin/javaws" "javaws" "/usr/local/java/jdk1.8.0_40/jre/bin/javaws" 1
	>$ sudo update-alternatives --set java /usr/local/java/jdk1.8.0_40/jre/bin/java
	>$ sudo update-alternatives --set javaws /usr/local/java/jdk1.8.0_40/jre/bin/javaws

## 4.重启系统后才会生效，也可以使用以下命令使其立即生效：
	
	>$ source /etc/profile

