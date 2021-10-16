# tomcat
## References
* https://github.com/bachmeb/tomcat-aws


##### Ask who am I?
```
whoami
```    
##### Check the value of the home directory environment variable
```
echo $HOME
```
##### Go home
```
cd ~
```
##### Check the Linux distro version
```
cat /proc/version
```
> ```
> Linux version 5.13.4-200.fc34.x86_64 (mockbuild@bkernel01.iad2.fedoraproject.org) (gcc (GCC) 11.1.1 20210531 (Red Hat 11.1.1-3), GNU ld version 2.35.1-41.fc34) #1 SMP Tue Jul 20 20:27:29 UTC 2021

##### Check the hostname of the ec2 instance
```
hostname
```
> ```
> fedora

##### Check the DNS domain name of the ec2 instance
```
dnsdomainname
```
##### Check the internal IP address
```
ifconfig
```
##### Check the external IP address
```
wget http://ipinfo.io/ip -qO -
```
##### Show all of the environment variables
```
declare
```
##### Look for JAVA in the list of environmental variables
```
env | grep JAVA
```
##### Echo the current JAVA_HOME
```
echo $JAVA_HOME
```
##### Ask where is Java?
```
whereis java
```
##### Check the Java version
```
java -version
```
##### Search yum for openjdk
```
yum search openjdk
```	
##### Install the latest Open JDK version
```
sudo yum install java-latest-openjdk
```
> ```
> Last metadata expiration check: 0:06:58 ago on Sat 16 Oct 2021 12:59:35 PM EDT.
> Package java-latest-openjdk-1:16.0.1.0.9-4.rolling.fc34.x86_64 is already installed.
> Dependencies resolved.
> Nothing to do.
> Complete!

##### Update the latest version of Open JDK
```
sudo yum update java-latest-openjdk
```
> ```
> Last metadata expiration check: 0:08:14 ago on Sat 16 Oct 2021 12:59:35 PM EDT.
> Dependencies resolved.
> ================================================================================================================================
>  Package               Architecture                       Version                 Repository                            Size
> ================================================================================================================================
> Upgrading:
>  java-latest-openjdk            x86_64             1:17.0.0.0.35-1.rolling.fc34            updates                      229 k
>  java-latest-openjdk-headless   x86_64             1:17.0.0.0.35-1.rolling.fc34            updates                       40 M
> 
> Transaction Summary
> ================================================================================================================================
> Upgrade  2 Packages
> 
> Total download size: 40 M
> Is this ok [y/N]: 
> Downloading Packages:
> (1/2): java-latest-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64.rpm                                                                                                      158 kB/s | 229 kB     00:01    
> (2/2): java-latest-openjdk-headless-17.0.0.0.35-1.rolling.fc34.x86_64.rpm                                                                                             2.4 MB/s |  40 MB     00:16    
> --------------------------------------------------------------------------------------------------------------------------------
> Total                                                                                                                                                                 2.3 MB/s |  40 MB     00:17     
> Running transaction check
> Transaction check succeeded.
> Running transaction test
> Transaction test succeeded.
> Running transaction
>   Running scriptlet: java-latest-openjdk-headless-1:17.0.0.0.35-1.rolling.fc34.x86_64                                      1/1 
>   Preparing        :                                                                                                       1/1 
>   Upgrading        : java-latest-openjdk-headless-1:17.0.0.0.35-1.rolling.fc34.x86_64                                      1/4 
>   Running scriptlet: java-latest-openjdk-headless-1:17.0.0.0.35-1.rolling.fc34.x86_64                                      1/4 
>   Upgrading        : java-latest-openjdk-1:17.0.0.0.35-1.rolling.fc34.x86_64                                               2/4 
>   Running scriptlet: java-latest-openjdk-1:17.0.0.0.35-1.rolling.fc34.x86_64                                               2/4 
>   Cleanup          : java-latest-openjdk-1:16.0.1.0.9-4.rolling.fc34.x86_                                                  3/4 
>   Running scriptlet: java-latest-openjdk-1:16.0.1.0.9-4.rolling.fc34.x86_64                                                3/4 
>   Cleanup          : java-latest-openjdk-headless-1:16.0.1.0.9-4.rolling.fc34.x86_64                                                                                                              4/4 
>   Running scriptlet: java-latest-openjdk-headless-1:16.0.1.0.9-4.rolling.fc34.x86_64                                       4/4 
>   Running scriptlet: java-latest-openjdk-headless-1:17.0.0.0.35-1.rolling.fc34.x86_64                                                                                                             4/4 
>   Running scriptlet: java-latest-openjdk-1:17.0.0.0.35-1.rolling.fc34.x86_64                                                                                                                      4/4 
>   Running scriptlet: java-latest-openjdk-headless-1:16.0.1.0.9-4.rolling.fc34.x86_64                                                                                                              4/4 
>   Verifying        : java-latest-openjdk-1:17.0.0.0.35-1.rolling.fc34.x86_64                                                                                                                      1/4 
>   Verifying        : java-latest-openjdk-1:16.0.1.0.9-4.rolling.fc34.x86_64                                                                                                                       2/4 
>   Verifying        : java-latest-openjdk-headless-1:17.0.0.0.35-1.rolling.fc34.x86_64                                                                                                             3/4 
>   Verifying        : java-latest-openjdk-headless-1:16.0.1.0.9-4.rolling.fc34.x86_64                                                                                                              4/4 
> 
> Upgraded:
>   java-latest-openjdk-1:17.0.0.0.35-1.rolling.fc34.x86_64                                       java-latest-openjdk-headless-1:17.0.0.0.35-1.rolling.fc34.x86_64                                      
> 
> Complete!
> 

##### Check the java version
```
java -version
```

##### Tell Linux which java version to use
```
sudo /usr/sbin/alternatives --config java
```
> ```
> There are 2 programs which provide 'java'.
> 
>   Selection    Command
> -----------------------------------------------
> *+ 1           java-11-openjdk.x86_64 (/usr/lib/jvm/java-11-openjdk-11.0.11.0.9-5.fc34.x86_64/bin/java)
>    2           java-latest-openjdk.x86_64 (/usr/lib/jvm/java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64/bin/java)
> 
> Enter to keep the current selection[+], or type selection number: 2

##### Read the symlinks in /usr/lib/jvm/
```
ls -l /usr/lib/jvm/
```
> ```
> total 8
> lrwxrwxrwx. 1 root root   26 Jun 27 15:55 java -> /etc/alternatives/java_sdk
> lrwxrwxrwx. 1 root root   29 Jun 27 15:55 java-11 -> /etc/alternatives/java_sdk_11
> lrwxrwxrwx. 1 root root   37 Jun 27 15:55 java-11-openjdk -> /etc/alternatives/java_sdk_11_openjdk
> drwxr-xr-x. 7 root root 4096 Jul 22 20:34 java-11-openjdk-11.0.11.0.9-5.fc34.x86_64
> drwxr-xr-x. 5 root root 4096 Oct 16 13:11 java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64
> lrwxrwxrwx. 1 root root   34 Jun 27 15:55 java-openjdk -> /etc/alternatives/java_sdk_openjdk
> lrwxrwxrwx. 1 root root   21 Apr 23 06:57 jre -> /etc/alternatives/jre
> lrwxrwxrwx. 1 root root   24 Apr 23 06:57 jre-11 -> /etc/alternatives/jre_11
> lrwxrwxrwx. 1 root root   32 Apr 23 06:57 jre-11-openjdk -> /etc/alternatives/jre_11_openjdk
> lrwxrwxrwx. 1 root root   41 Jul  8 01:55 jre-11-openjdk-11.0.11.0.9-5.fc34.x86_64 -> java-11-openjdk-11.0.11.0.9-5.fc34.x86_64
> lrwxrwxrwx. 1 root root   24 Oct 16 13:11 jre-17 -> /etc/alternatives/jre_17
> lrwxrwxrwx. 1 root root   32 Oct 16 13:11 jre-17-openjdk -> /etc/alternatives/jre_17_openjdk
> lrwxrwxrwx. 1 root root   49 Sep 14 20:40 jre-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64 -> java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64
> lrwxrwxrwx. 1 root root   29 Apr 23 06:57 jre-openjdk -> /etc/alternatives/jre_openjdk

##### Confirm that /etc/alternatives/jre points to the latest openjdk version
```
ls -la /etc/alternatives/jre
```
> ```
> lrwxrwxrwx. 1 root root 62 Oct 16 13:15 /etc/alternatives/jre -> /usr/lib/jvm/java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64

##### Check the java version
```
java -version
```
> ```
> openjdk version "17" 2021-09-14
> OpenJDK Runtime Environment 21.9 (build 17+35)
> OpenJDK 64-Bit Server VM 21.9 (build 17+35, mixed mode, sharing)

##### Check the Java compiler version
```
javac -version
```
> ```
> javac 11.0.11

##### Install the latest java compiler version
```
sudo yum install java-latest-openjdk-devel
```
> Last metadata expiration check: 0:38:10 ago on Sat 16 Oct 2021 12:59:35 PM EDT.
> Dependencies resolved.
> ============================================================================================================
>  Package                          Architecture  Version                                Repository      Size
> ============================================================================================================
> Installing:
>  java-latest-openjdk-devel        x86_64        1:17.0.0.0.35-1.rolling.fc34           updates        4.7 M
> 
> Transaction Summary
> ============================================================================================================
> Install  1 Package
> 
> Total download size: 4.7 M
> Installed size: 8.9 M
> Is this ok [y/N]: y
> Downloading Packages:
> java-latest-openjdk-devel-17.0.0.0.35-1.rolling.fc34.x86_64.rpm             2.0 MB/s | 4.7 MB     00:02    
> ------------------------------------------------------------------------------------------------------------
> Total                                                                       1.5 MB/s | 4.7 MB     00:03     
> Running transaction check
> Transaction check succeeded.
> Running transaction test
> Transaction test succeeded.
> Running transaction
>   Preparing        :                                                                                    1/1 
>   Installing       : java-latest-openjdk-devel-1:17.0.0.0.35-1.rolling.fc34.x86_64                      1/1 
>   Running scriptlet: java-latest-openjdk-devel-1:17.0.0.0.35-1.rolling.fc34.x86_64                      1/1 
>   Verifying        : java-latest-openjdk-devel-1:17.0.0.0.35-1.rolling.fc34.x86_64                      1/1 
> 
> Installed:
>   java-latest-openjdk-devel-1:17.0.0.0.35-1.rolling.fc34.x86_64                                             
> 
> Complete!


##### Tell Linux which Java compiler to use
```
sudo /usr/sbin/alternatives --config javac
```
> ```
> sudo /usr/sbin/alternatives --config javac
> 
> There are 2 programs which provide 'javac'.
> 
>   Selection    Command
> -----------------------------------------------
> *+ 1           java-11-openjdk.x86_64 (/usr/lib/jvm/java-11-openjdk-11.0.11.0.9-5.fc34.x86_64/bin/javac)
>    2           java-latest-openjdk.x86_64 (/usr/lib/jvm/java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64/bin/javac)
> 
> Enter to keep the current selection[+], or type selection number: 2

##### Confirm that /usr/lib/jvm/java points to /etc/alternatives/java_sdk
```
ls -l /usr/lib/jvm/java
```
> ```
> lrwxrwxrwx. 1 root root 26 Jun 27 15:55 /usr/lib/jvm/java -> /etc/alternatives/java_sdk

##### Confirm that /etc/alternatives/java_sdk points to the installation directory for the latest jdk version
```
ls -l /etc/alternatives/java_sdk
```
> ```
> lrwxrwxrwx. 1 root root 62 Oct 16 13:40 /etc/alternatives/java_sdk -> /usr/lib/jvm/java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64

##### List the contents of the jdk installation directory
```
ls -la /usr/lib/jvm/java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64
```
> ```
> total 36
> drwxr-xr-x.  7 root root 4096 Oct 16 13:38 .
> drwxr-xr-x.  4 root root 4096 Oct 16 13:38 ..
> drwxr-xr-x.  2 root root 4096 Oct 16 13:38 bin
> lrwxrwxrwx.  1 root root   80 Sep 14 20:40 conf -> /etc/java/java-17-openjdk/java-17-openjdk-17.0.0.0.35-1.rolling.fc34.x86_64/conf
> drwxr-xr-x.  3 root root 4096 Oct 16 13:38 include
> drwxr-xr-x. 72 root root 4096 Oct 16 13:11 legal
> drwxr-xr-x.  4 root root 4096 Oct 16 13:38 lib
> -rw-r--r--.  1 root root 1209 Sep 14 20:25 release
> drwxr-xr-x.  2 root root 4096 Oct 16 13:38 tapset

##### Echo the $JAVA_HOME environment variable
```
echo $JAVA_HOME
```
> ```
> 

##### Set the JAVA_HOME environment variable to the Open JDK directory
```
export JAVA_HOME='/usr/lib/jvm/java'
```

##### Echo the $JAVA_HOME environment variable
```
echo $JAVA_HOME
```
> ```
> /usr/lib/jvm/java

##### List the available tomcat packages in yum
```
yum --enablerepo="*" list available | grep tomcat
```
> ```
> yum list available | grep tomcat
> tomcat.noarch                                                                            1:9.0.53-1.fc34                                                  updates              
> tomcat-admin-webapps.noarch                                                              1:9.0.53-1.fc34                                                  updates              
> tomcat-docs-webapp.noarch                                                                1:9.0.53-1.fc34                                                  updates              
> tomcat-el-3.0-api.noarch                                                                 1:9.0.53-1.fc34                                                  updates              
> tomcat-jsp-2.3-api.noarch                                                                1:9.0.53-1.fc34                                                  updates              
> tomcat-jsvc.noarch                                                                       1:9.0.53-1.fc34                                                  updates              
> tomcat-lib.noarch                                                                        1:9.0.53-1.fc34                                                  updates              
> tomcat-native.x86_64                                                                     1.2.23-4.fc34                                                    fedora               
> tomcat-servlet-4.0-api.noarch                                                            1:9.0.53-1.fc34                                                  updates              
> tomcat-taglibs-parent.noarch                                                             3-14.fc34                                                        fedora               
> tomcat-taglibs-standard.noarch                                                           1.2.5-13.fc34                                                    fedora               
> tomcat-taglibs-standard-javadoc.noarch                                                   1.2.5-13.fc34                                                    fedora               
> tomcat-webapps.noarch                                                                    1:9.0.53-1.fc34                                                  updates              
> tomcatjss.noarch                                                                         7.6.1-2.fc34                                                     fedora               
> 

##### Search yum for tomcat
```
yum search tomcat
```
> ```
> Last metadata expiration check: 3:20:32 ago on Sat 16 Oct 2021 10:38:26 AM EDT.
> ==================================== Name Exactly Matched: tomcat =======================================
> tomcat.noarch : Apache Servlet/JSP Engine, RI for Servlet 4.0/JSP 2.3 API
> =================================== Name & Summary Matched: tomcat ======================================
> tomcat-admin-webapps.noarch : The host-manager and manager web applications for Apache Tomcat
> tomcat-docs-webapp.noarch : The docs web application for Apache Tomcat
> tomcat-el-3.0-api.noarch : Apache Tomcat Expression Language v3.0 API Implementation Classes
> tomcat-jsp-2.3-api.noarch : Apache Tomcat JavaServer Pages v2.3 API Implementation Classes
> tomcat-jsvc.noarch : Apache jsvc wrapper for Apache Tomcat as separate service
> tomcat-lib.noarch : Libraries needed to run the Tomcat Web container
> tomcat-native.x86_64 : Tomcat native library
> tomcat-servlet-4.0-api.noarch : Apache Tomcat Java Servlet v4.0 API Implementation Classes
> tomcat-taglibs-standard-javadoc.noarch : Javadoc for tomcat-taglibs-standard
> tomcat-webapps.noarch : The ROOT and examples web applications for Apache Tomcat
> tomcatjss.noarch : JSS Connector for Apache Tomcat
> ======================================== Name Matched: tomcat ===========================================
> tomcat-taglibs-parent.noarch : Apache Taglibs Parent
> tomcat-taglibs-standard.noarch : Apache Standard Taglib
> ======================================= Summary Matched: tomcat =========================================
> mod_cluster.x86_64 : Apache HTTP Server dynamic load balancer with Wildfly and Tomcat libraries


##### Install Tomcat
```
sudo yum install tomcat tomcat-webapps tomcat-admin-webapps
```
> ```
> sudo yum install tomcat tomcat-webapps tomcat-admin-webapps
> Last metadata expiration check: 1:01:19 ago on Sat 16 Oct 2021 12:59:35 PM EDT.
> Dependencies resolved.
> =====================================================================================================
>  Package                          Architecture    Version                     Repository        Size
> =====================================================================================================
> Installing:
>  tomcat                           noarch          1:9.0.53-1.fc34             updates           89 k
>  tomcat-admin-webapps             noarch          1:9.0.53-1.fc34             updates           72 k
>  tomcat-webapps                   noarch          1:9.0.53-1.fc34             updates          311 k
> Installing dependencies:
>  apache-commons-daemon            x86_64          1.2.4-1.fc34                fedora            55 k
>  ecj                              noarch          1:4.19-1.fc34               fedora           2.8 M
>  tomcat-el-3.0-api                noarch          1:9.0.53-1.fc34             updates          104 k
>  tomcat-jsp-2.3-api               noarch          1:9.0.53-1.fc34             updates           63 k
>  tomcat-lib                       noarch          1:9.0.53-1.fc34             updates          5.4 M
>  tomcat-servlet-4.0-api           noarch          1:9.0.53-1.fc34             updates          281 k
>  tomcat-taglibs-standard          noarch          1.2.5-13.fc34               fedora           409 k
> Installing weak dependencies:
>  tomcat-native                    x86_64          1.2.23-4.fc34               fedora            82 k
> 
> Transaction Summary
> =====================================================================================================
> Install  11 Packages
> 
> Total download size: 9.6 M
> Installed size: 12 M
> Is this ok [y/N]: y

##### Ask where is tomcat?
```
whereis tomcat
```
> ```
> tomcat: /usr/sbin/tomcat /etc/tomcat /usr/libexec/tomcat /usr/share/tomcat

##### Get a listing of the Catalina Base directory
```
ls -l /usr/share/tomcat/
```
> ```    
> total 4
> drwxr-xr-x. 2 root root   4096 Oct 16 14:01 bin
> lrwxrwxrwx. 1 root tomcat   11 Sep 16 06:30 conf -> /etc/tomcat
> lrwxrwxrwx. 1 root tomcat   22 Sep 16 06:30 lib -> /usr/share/java/tomcat
> lrwxrwxrwx. 1 root tomcat   15 Sep 16 06:30 logs -> /var/log/tomcat
> lrwxrwxrwx. 1 root tomcat   22 Sep 16 06:30 temp -> /var/cache/tomcat/temp
> lrwxrwxrwx. 1 root tomcat   23 Sep 16 06:30 webapps -> /var/lib/tomcat/webapps
> lrwxrwxrwx. 1 root tomcat   22 Sep 16 06:30 work -> /var/cache/tomcat/work

##### Check what is listening on port 8080
```
sudo lsof -ni:8080
```    
##### Check the status of the tomcat service
```
sudo service tomcat status
```
> ```
> Redirecting to /bin/systemctl status tomcat.service
> ○ tomcat.service - Apache Tomcat Web Application Container
>      Loaded: loaded (/usr/lib/systemd/system/tomcat.service; disabled; vendor preset: disabled)
>      Active: inactive (dead)

##### Start the tomcat service
```
sudo service tomcat start
```
> ```
> Redirecting to /bin/systemctl start tomcat.service

##### Check the status of the tomcat service
```
sudo service tomcat status
```
> ```
> Redirecting to /bin/systemctl status tomcat.service
> ● tomcat.service - Apache Tomcat Web Application Container
>      Loaded: loaded (/usr/lib/systemd/system/tomcat.service; disabled; vendor preset: disabled)
>      Active: active (running) since Sat 2021-10-16 14:06:05 EDT; 2min 1s ago
>    Main PID: 109201 (java)
>       Tasks: 26 (limit: 4517)
>      Memory: 148.6M
>         CPU: 7.639s
>      CGroup: /system.slice/tomcat.service
>              └─109201 /usr/lib/jvm/jre/bin/java -agentpath:/usr/lib/abrt-java-connector/libabrt-java>
> 
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.453 INFO [main] org.apache.jasper.servle>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.457 INFO [main] org.apache.catalina.star>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.458 INFO [main] org.apache.catalina.star>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.697 INFO [main] org.apache.jasper.servle>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.725 INFO [main] org.apache.catalina.star>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.726 INFO [main] org.apache.catalina.star>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.961 INFO [main] org.apache.jasper.servle>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.967 INFO [main] org.apache.catalina.star>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.972 INFO [main] org.apache.coyote.Abstra>
> Oct 16 14:06:10 fedora server[109201]: 16-Oct-2021 14:06:10.991 INFO [main] org.apache.catalina.star>


##### Grep the output of the process status command for tomcat
```
ps -ef | grep tomcat
```
> ```
> tomcat    109201       1  2 14:06 ?        00:00:08 /usr/lib/jvm/jre/bin/java -agentpath:/usr/lib/abrt-java-connector/libabrt-java-connector.so=abrt=on, -Djavax.sql.DataSource.Factory=org.apache.commons.dbcp.BasicDataSourceFactory -classpath /usr/share/tomcat/bin/bootstrap.jar:/usr/share/tomcat/bin/tomcat-juli.jar:/usr/lib/java/commons-daemon.jar -Dcatalina.base=/usr/share/tomcat -Dcatalina.home=/usr/share/tomcat -Djava.endorsed.dirs= -Djava.io.tmpdir=/var/cache/tomcat/temp -Djava.util.logging.config.file=/usr/share/tomcat/conf/logging.properties -Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager org.apache.catalina.startup.Bootstrap start

##### Check what is listening on port 8080
```
sudo lsof -ni:8080
```
> ```
> COMMAND    PID   USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
> java    109201 tomcat   44u  IPv6 759216      0t0  TCP *:webcache (LISTEN)

##### Install Lynx
```
sudo yum install lynx
```
##### Go to the Tomcat welcome page
```
lynx localhost:8080
```
> ```
>                                              Apache Tomcat/9.0.53 (p1 of 3)
>    Home Documentation Configuration Examples Wiki Mailing Lists Find Help
> 
> Apache Tomcat/9.0.53
> 
> If you're seeing this, you've successfully installed Tomcat. Congratulations!
> 
>    [tomcat logo]
> 
> Recommended Reading:
> 
> Security Considerations How-To
> 
> Manager Application How-To
> 
> Clustering/Session Replication How-To
> 
>    Server Status
>    Manager App
>    Host Manager
> 
> Developer Quick Start

  
##### List the contents of the Tomcat logs directory
```
sudo ls -l /usr/share/tomcat/logs/
```
> ```
> total 16
> -rw-r--r--. 1 tomcat tomcat 7989 Oct 16 14:06 catalina.2021-10-16.log
> -rw-r--r--. 1 tomcat tomcat    0 Oct 16 14:06 host-manager.2021-10-16.log
> -rw-r--r--. 1 tomcat tomcat  408 Oct 16 14:06 localhost.2021-10-16.log
> -rw-r--r--. 1 tomcat tomcat  152 Oct 16 14:17 localhost_access_log.2021-10-16.txt
> -rw-r--r--. 1 tomcat tomcat    0 Oct 16 14:06 manager.2021-10-16.log
	
##### Read the catalina.out file
```
sudo cat /usr/share/tomcat/logs/catalina.2021-10-16.log
```
##### Read the localhost access log
```
sudo find /usr/share/tomcat/logs/ -name localhost* -exec cat {} \;
```
> ```
> 16-Oct-2021 14:06:09.754 INFO [main] org.apache.catalina.core.ApplicationContext.log ContextListener: contextInitialized()
> 16-Oct-2021 14:06:09.754 INFO [main] org.apache.catalina.core.ApplicationContext.log SessionListener: contextInitialized()
> 16-Oct-2021 14:06:09.756 INFO [main] org.apache.catalina.core.ApplicationContext.log ContextListener: attributeAdded('StockTicker', 'async.Stockticker@42f22995')
> 0:0:0:0:0:0:0:1 - - [16/Oct/2021:14:14:11 -0400] "GET / HTTP/1.0" 200 11136
> 0:0:0:0:0:0:0:1 - - [16/Oct/2021:14:17:21 -0400] "GET / HTTP/1.1" 200 11156

##### Set tomcat to start on run level 3
```
chkconfig
```
```
chkconfig | grep tomcat
```
```
sudo chkconfig tomcat on 
```
> ```
> Note: Forwarding request to 'systemctl enable tomcat.service'.
> Created symlink /etc/systemd/system/multi-user.target.wants/tomcat.service → /usr/lib/systemd/system/tomcat.service.

```
ls -l /etc/systemd/system/multi-user.target.wants/tomcat.service
```
> ```
> lrwxrwxrwx. 1 root root 38 Oct 16 14:25 /etc/systemd/system/multi-user.target.wants/tomcat.service -> /usr/lib/systemd/system/tomcat.service




##### Read the Tomcat config file
```
less /usr/share/tomcat/conf/tomcat.conf
```
*This file is where the CATALINA_BASE and CATALINA_HOME environment variables are set*    

##### Read the Tomcat init file
```
less /etc/init.d/tomcat
```
##### Read the Tomcat launch script
```
less /usr/sbin/tomcat
```
##### Read the server.xml file
```
less /usr/share/tomcat/conf/server.xml
```
##### Read the web.xml file
```
less /usr/share/tomcat/conf/web.xml 
```
##### grep the contents of the passwd file to see that a user named tomcat has been created
```
cat /etc/passwd |grep tomcat
```    
##### Add users to the Tomcat users file
```
sudo vim /usr/share/tomcat/conf/tomcat-users.xml
```
```xml
<?xml version='1.0' encoding='utf-8'?>
<tomcat-users>

  <role rolename="manager-script" />
  <role rolename="admin-script" />
  <user username="abc" password="123" roles="manager-script,admin-script" />

</tomcat-users>
```
##### Restart the Tomcat service to pick up the changes to tomcat-users.xml
```
sudo service tomcat restart
```	
##### Check environment variable for home directory
```
echo $HOME
```    
##### Create a Build Properties file in your home directory
```
cd ~
pwd
vi build.properties
```
##### Add Catalina home, app name, manager username and password to the build.properties file
*These values are used by the build.xml file*  
```
catalina.home=/usr/share/tomcat
app.name=hello
manager.username=abc
manager.password=123
```
##### Install git
```
sudo yum install git
```	
##### Create project folder
```
mkdir -p ~/git/tc-aws
```
##### Make a .gitignore file
```
cd git/tc-aws
nano .gitignore
```
```
*.class

# Mobile Tools for Java (J2ME)
.mtj.tmp/

# Package Files #
*.jar
*.war
*.ear

# virtual machine crash logs, see http://www.java.com/en/download/help/error_hotspot.xml
hs_err_pid*

# AWS 
*.pem

# Tomcat 
build.properties

# Ant
build/
dist/
```
##### Initialize project repository
```
git init
```
##### Create remote repository
```
http://github.com/
```
##### Configure repository
```
git config user.name {username}
git config user.email {emailaddress@example.com}
```
##### Add remote origin to local repository
```
git remote add origin http://github.com/{username}/{projectname}.git
```
##### Pull from remote
```
git pull origin master
```
##### Check status
```
git status
```    
##### Push to remote
```
git push --set-upstream origin master
```
##### Create Build XML File
```
cd ~/git/tc-aws
wget https://tomcat.apache.org/tomcat-7.0-doc/appdev/build.xml.txt
cp build.xml.txt build.xml
nano build.xml
```
*Give the project a name in the project declaration*  
*Set the app.name in build.properties*  
*Set catalina.home in build.properties*  
*Add includeantruntime="false" to the javac declaration*  
```xml
<!--
  Licensed to the Apache Software Foundation (ASF) under one or more
  contributor license agreements.  See the NOTICE file distributed with
  this work for additional information regarding copyright ownership.
  The ASF licenses this file to You under the Apache License, Version 2.0
  (the "License"); you may not use this file except in compliance with
  the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.
-->

<!--
     General purpose build script for web applications and web services,
     including enhanced support for deploying directly to a Tomcat
     based server.

     This build script assumes that the source code of your web application
     is organized into the following subdirectories underneath the source
     code directory from which you execute the build script:

        docs                 Static documentation files to be copied to
                             the "docs" subdirectory of your distribution.

        src                  Java source code (and associated resource files)
                             to be compiled to the "WEB-INF/classes"
                             subdirectory of your web application.

        web                  Static HTML, JSP, and other content (such as
                             image files), including the WEB-INF subdirectory
                             and its configuration file contents.
-->


<!-- A "project" describes a set of targets that may be requested
     when Ant is executed.  The "default" attribute defines the
     target which is executed if no specific target is requested,
     and the "basedir" attribute defines the current working directory
     from which Ant executes the requested task.  This is normally
     set to the current working directory.
-->

<project name="MY PROJECT NAME" default="compile" basedir="."><!-- UPDATE THIS! -->



<!-- ===================== Property Definitions =========================== -->


<!--

  Each of the following properties are used in the build script.
  Values for these properties are set by the first place they are
  defined, from the following list:

  * Definitions on the "ant" command line (ant -Dfoo=bar compile).

  * Definitions from a "build.properties" file in the top level
    source directory of this application.

  * Definitions from a "build.properties" file in the developer's
    home directory.

  * Default definitions in this build.xml file.

  You will note below that property values can be composed based on the
  contents of previously defined properties.  This is a powerful technique
  that helps you minimize the number of changes required when your development
  environment is modified.  Note that property composition is allowed within
  "build.properties" files as well as in the "build.xml" script.

-->

  <property file="build.properties"/>
  <property file="${user.home}/build.properties"/>


<!-- ==================== File and Directory Names ======================== -->


<!--

  These properties generally define file and directory names (or paths) that
  affect where the build process stores its outputs.

  app.name             Base name of this application, used to
                       construct filenames and directories.
                       Defaults to "myapp".

  app.path             Context path to which this application should be
                       deployed (defaults to "/" plus the value of the
                       "app.name" property).

  app.version          Version number of this iteration of the application.

  build.home           The directory into which the "prepare" and
                       "compile" targets will generate their output.
                       Defaults to "build".

  catalina.home        The directory in which you have installed
                       a binary distribution of Tomcat.  This will
                       be used by the "deploy" target.

  dist.home            The name of the base directory in which
                       distribution files are created.
                       Defaults to "dist".

  manager.password     The login password of a user that is assigned the
                       "manager-script" role (so that he or she can execute
                       commands via the "/manager" web application)

  manager.url          The URL of the "/manager" web application on the
                       Tomcat installation to which we will deploy web
                       applications and web services.

  manager.username     The login username of a user that is assigned the
                       "manager-script" role (so that he or she can execute
                       commands via the "/manager" web application)

-->

  <!-- <property name="catalina.home" value="../../../.."/>--> <!-- COMMENT OUT -->
  <!--<property name="app.name"      value="myapp"/>--><!-- SET IN BUILD PROPERTIES FILE -->
  
  <property name="app.path"      value="/${app.name}"/>
  <property name="app.version"   value="0.1-dev"/>
  
  <property name="build.home"    value="${basedir}/build"/>
  <property name="dist.home"     value="${basedir}/dist"/>
  <property name="docs.home"     value="${basedir}/docs"/>
  <property name="src.home"      value="${basedir}/src"/>
  <property name="web.home"      value="${basedir}/web"/>
  
  <property name="manager.url"   value="http://localhost:8080/manager/text"/>

<!-- ==================== External Dependencies =========================== -->


<!--

  Use property values to define the locations of external JAR files on which
  your application will depend.  In general, these values will be used for
  two purposes:
  * Inclusion on the classpath that is passed to the Javac compiler
  * Being copied into the "/WEB-INF/lib" directory during execution
    of the "deploy" target.

  Because we will automatically include all of the Java classes that Tomcat
  exposes to web applications, we will not need to explicitly list any of those
  dependencies.  You only need to worry about external dependencies for JAR
  files that you are going to include inside your "/WEB-INF/lib" directory.

-->

<!-- Dummy external dependency -->
<!--
  <property name="foo.jar"
           value="/path/to/foo.jar"/>
-->


<!-- ==================== Compilation Classpath =========================== -->

<!--

  Rather than relying on the CLASSPATH environment variable, Ant includes
  features that makes it easy to dynamically construct the classpath you
  need for each compilation.  The example below constructs the compile
  classpath to include the servlet.jar file, as well as the other components
  that Tomcat makes available to web applications automatically, plus anything
  that you explicitly added.

-->

  <path id="compile.classpath">

    <!-- Include all JAR files that will be included in /WEB-INF/lib -->
    <!-- *** CUSTOMIZE HERE AS REQUIRED BY YOUR APPLICATION *** -->
<!--
    <pathelement location="${foo.jar}"/>
-->

    <!-- Include all elements that Tomcat exposes to applications -->
    <fileset dir="${catalina.home}/bin">
      <include name="*.jar"/>
    </fileset>
    <pathelement location="${catalina.home}/lib"/>
    <fileset dir="${catalina.home}/lib">
      <include name="*.jar"/>
    </fileset>

  </path>



<!-- ================== Custom Ant Task Definitions ======================= -->


<!--

  These properties define custom tasks for the Ant build tool that interact
  with the "/manager" web application installed with Tomcat.  Before they
  can be successfully utilized, you must perform the following steps:

  - Copy the file "lib/catalina-ant.jar" from your Tomcat
    installation into the "lib" directory of your Ant installation.

  - Create a "build.properties" file in your application's top-level
    source directory (or your user login home directory) that defines
    appropriate values for the "manager.password", "manager.url", and
    "manager.username" properties described above.

  For more information about the Manager web application, and the functionality
  of these tasks, see <http://localhost:8080/tomcat-docs/manager-howto.html>.

-->

  <taskdef resource="org/apache/catalina/ant/catalina.tasks"
           classpathref="compile.classpath"/>


<!--  ==================== Compilation Control Options ==================== -->

<!--

  These properties control option settings on the Javac compiler when it
  is invoked using the <javac> task.

  compile.debug        Should compilation include the debug option?

  compile.deprecation  Should compilation include the deprecation option?

  compile.optimize     Should compilation include the optimize option?

-->

  <property name="compile.debug"       value="true"/>
  <property name="compile.deprecation" value="false"/>
  <property name="compile.optimize"    value="true"/>



<!-- ==================== All Target ====================================== -->

<!--

  The "all" target is a shortcut for running the "clean" target followed
  by the "compile" target, to force a complete recompile.

-->

  <target name="all" depends="clean,compile"
   description="Clean build and dist directories, then compile"/>



<!-- ==================== Clean Target ==================================== -->

<!--

  The "clean" target deletes any previous "build" and "dist" directory,
  so that you can be ensured the application can be built from scratch.

-->

  <target name="clean"
   description="Delete old build and dist directories">
    <delete dir="${build.home}"/>
    <delete dir="${dist.home}"/>
  </target>



<!-- ==================== Compile Target ================================== -->

<!--

  The "compile" target transforms source files (from your "src" directory)
  into object files in the appropriate location in the build directory.
  This example assumes that you will be including your classes in an
  unpacked directory hierarchy under "/WEB-INF/classes".

-->

  <target name="compile" depends="prepare"
   description="Compile Java sources">

    <!-- Compile Java classes as necessary -->
    <mkdir dir="${build.home}/WEB-INF/classes"/>
    
    <javac srcdir="${src.home}"
    	destdir="${build.home}/WEB-INF/classes"
    	debug="${compile.debug}"
    	deprecation="${compile.deprecation}"
      	optimize="${compile.optimize}"
      	includeantruntime="false"
        ><!-- ADD includeantruntime="false" -->
        <classpath refid="compile.classpath"/>
    </javac>

    <!-- Copy application resources -->
    <copy  todir="${build.home}/WEB-INF/classes">
      <fileset dir="${src.home}" excludes="**/*.java"/>
    </copy>

  </target>



<!-- ==================== Dist Target ===================================== -->


<!--

  The "dist" target creates a binary distribution of your application
  in a directory structure ready to be archived in a tar.gz or zip file.
  Note that this target depends on two others:

  * "compile" so that the entire web application (including external
    dependencies) will have been assembled

  * "javadoc" so that the application Javadocs will have been created

-->

  <target name="dist" depends="compile,javadoc"
   description="Create binary distribution">

    <!-- Copy documentation subdirectories -->
    <mkdir   dir="${dist.home}/docs"/>
    <copy    todir="${dist.home}/docs">
      <fileset dir="${docs.home}"/>
    </copy>

    <!-- Create application JAR file -->
    <jar jarfile="${dist.home}/${app.name}-${app.version}.war"
         basedir="${build.home}"/>

    <!-- Copy additional files to ${dist.home} as necessary -->

  </target>



<!-- ==================== Install Target ================================== -->

<!--

  The "install" target tells the specified Tomcat installation to dynamically
  install this web application and make it available for execution.  It does
  *not* cause the existence of this web application to be remembered across
  Tomcat restarts; if you restart the server, you will need to re-install all
  this web application.

  If you have already installed this application, and simply want Tomcat to
  recognize that you have updated Java classes (or the web.xml file), use the
  "reload" target instead.

  NOTE:  This target will only succeed if it is run from the same server that
  Tomcat is running on.

  NOTE:  This is the logical opposite of the "remove" target.

-->

  <target name="install" depends="compile"
   description="Install application to servlet container">

    <deploy url="${manager.url}"
       username="${manager.username}"
       password="${manager.password}"
           path="${app.path}"
       localWar="file://${build.home}"/>

  </target>


<!-- ==================== Javadoc Target ================================== -->

<!--

  The "javadoc" target creates Javadoc API documentation for the Java
  classes included in your application.  Normally, this is only required
  when preparing a distribution release, but is available as a separate
  target in case the developer wants to create Javadocs independently.

-->

  <target name="javadoc" depends="compile"
   description="Create Javadoc API documentation">

    <mkdir          dir="${dist.home}/docs/api"/>
    <javadoc sourcepath="${src.home}"
                destdir="${dist.home}/docs/api"
           packagenames="*">
      <classpath refid="compile.classpath"/>
    </javadoc>

  </target>



<!-- ====================== List Target =================================== -->

<!--

  The "list" target asks the specified Tomcat installation to list the
  currently running web applications, either loaded at startup time or
  installed dynamically.  It is useful to determine whether or not the
  application you are currently developing has been installed.

-->

  <target name="list"
   description="List installed applications on servlet container">

    <list    url="${manager.url}"
        username="${manager.username}"
        password="${manager.password}"/>

  </target>


<!-- ==================== Prepare Target ================================== -->

<!--

  The "prepare" target is used to create the "build" destination directory,
  and copy the static contents of your web application to it.  If you need
  to copy static files from external dependencies, you can customize the
  contents of this task.

  Normally, this task is executed indirectly when needed.

-->

  <target name="prepare">

    <!-- Create build directories as needed -->
    <mkdir  dir="${build.home}"/>
    <mkdir  dir="${build.home}/WEB-INF"/>
    <mkdir  dir="${build.home}/WEB-INF/classes"/>


    <!-- Copy static content of this web application -->
    <copy todir="${build.home}">
      <fileset dir="${web.home}"/>
    </copy>

    <!-- Copy external dependencies as required -->
    <!-- *** CUSTOMIZE HERE AS REQUIRED BY YOUR APPLICATION *** -->
    <mkdir  dir="${build.home}/WEB-INF/lib"/>
<!--
    <copy todir="${build.home}/WEB-INF/lib" file="${foo.jar}"/>
-->

    <!-- Copy static files from external dependencies as needed -->
    <!-- *** CUSTOMIZE HERE AS REQUIRED BY YOUR APPLICATION *** -->

  </target>


<!-- ==================== Reload Target =================================== -->

<!--

  The "reload" signals the specified application Tomcat to shut itself down
  and reload. This can be useful when the web application context is not
  reloadable and you have updated classes or property files in the
  /WEB-INF/classes directory or when you have added or updated jar files in the
  /WEB-INF/lib directory.

  NOTE: The /WEB-INF/web.xml web application configuration file is not reread
  on a reload. If you have made changes to your web.xml file you must stop
  then start the web application.

-->

  <target name="reload" depends="compile"
   description="Reload application on servlet container">

    <reload url="${manager.url}"
       username="${manager.username}"
       password="${manager.password}"
           path="${app.path}"/>

  </target>


<!-- ==================== Remove Target =================================== -->

<!--

  The "remove" target tells the specified Tomcat installation to dynamically
  remove this web application from service.

  NOTE:  This is the logical opposite of the "install" target.

-->

  <target name="remove"
   description="Remove application on servlet container">

    <undeploy url="${manager.url}"
         username="${manager.username}"
         password="${manager.password}"
             path="${app.path}"/>

  </target>

</project>
```

##### Install ant
    sudo yum install ant

##### List installed projects
    ant -v list
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `list' is [list]
Complete build sequence is [list, prepare, compile, reload, install, remove, javadoc, clean, dist, all, ]

list:
     [list] OK - Listed applications for virtual host localhost
     [list] /manager:running:1:manager
     [list] /:running:0:ROOT
     [list] /sample:running:0:sample
     [list] /examples:running:0:examples
     [list] /host-manager:running:0:host-manager

BUILD SUCCESSFUL
Total time: 0 seconds

```
    
##### Make a web directory in the project folder
	mkdir web

##### Prepare the project
	ant -v prepare
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `prepare' is [prepare]
Complete build sequence is [prepare, compile, reload, install, remove, list, javadoc, clean, dist, all, ]

prepare:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
     [copy] No sources found.
     [copy]  added as  is outdated.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/lib because it already exists.

BUILD SUCCESSFUL
Total time: 0 seconds
```

##### Make a src directory in the project folder
	mkdir src
	
##### Compile the project
    ant -v compile
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `compile' is [prepare, compile]
Complete build sequence is [prepare, compile, reload, install, remove, list, javadoc, clean, dist, all, ]

prepare:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
     [copy] No sources found.
     [copy]  added as  is outdated.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/lib because it already exists.

compile:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
    [javac] No sources found.
     [copy] No sources found.
     [copy]  added as  is outdated.

BUILD SUCCESSFUL
Total time: 0 seconds
```

##### Recursively change the mode of all the files in the project directory
```
chmod -R 775 ~/git/tc-aws
```
##### Install the project
    ant -v install
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `install' is [prepare, compile, install]
Complete build sequence is [prepare, compile, install, reload, remove, list, javadoc, clean, dist, all, ]

prepare:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
     [copy] No sources found.
     [copy]  added as  is outdated.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/lib because it already exists.

compile:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
    [javac] No sources found.
     [copy] No sources found.
     [copy]  added as  is outdated.

install:
   [deploy] OK - Deployed application at context path /hello

BUILD SUCCESSFUL
Total time: 1 second
```

##### Reload the project
    ant -v reload
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `reload' is [prepare, compile, reload]
Complete build sequence is [prepare, compile, reload, install, remove, list, javadoc, clean, dist, all, ]

prepare:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF because it already exists.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
     [copy] No sources found.
     [copy]  added as  is outdated.
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/lib because it already exists.

compile:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
    [javac] No sources found.
     [copy] No sources found.
     [copy]  added as  is outdated.

reload:
   [reload] OK - Reloaded application at context path /hello

BUILD SUCCESSFUL
Total time: 0 seconds
```

##### Remove the project
    ant -v remove
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `remove' is [remove]
Complete build sequence is [remove, prepare, compile, reload, install, list, javadoc, clean, dist, all, ]

remove:
 [undeploy] OK - Undeployed application at context path /hello

BUILD SUCCESSFUL
Total time: 1 second
```

##### Clean the project build directory
    ant -v clean
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `clean' is [clean]
Complete build sequence is [clean, prepare, compile, reload, install, remove, list, javadoc, dist, all, ]

clean:
   [delete] Deleting directory /home/bachmeb/git/tc-aws/build
   [delete] Deleting directory /home/bachmeb/git/tc-aws/build/WEB-INF/classes
   [delete] Deleting directory /home/bachmeb/git/tc-aws/build/WEB-INF/lib
   [delete] Deleting directory /home/bachmeb/git/tc-aws/build/WEB-INF
   [delete] Deleting directory /home/bachmeb/git/tc-aws/build

BUILD SUCCESSFUL
Total time: 0 seconds
```

##### Create an index file
    cd web
    vim index.html
```xml
Hello <a href="./there">There</a>.
```
##### Make a Java class
    mkdir -p ~/git/tc-aws/src/com/example/greeting
    vim ~/git/tc-aws/src/com/example/greeting/HelloServlet.java
```java
package com.example.packname;

import java.io.IOException;
import java.io.PrintWriter;

import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * Simple servlet displays a message
 */
public class HelloServlet extends HttpServlet {

    @Override
    public void doGet(HttpServletRequest request, HttpServletResponse
            response) throws IOException {
        PrintWriter out = response.getWriter();
        out.println("HELLO!!!");
        out.close();
    }
}
```

##### Create a web.xml file
    mkdir -p ~/git/tc-aws/web/WEB-INF
    vim ~/git/tc-aws/web/WEB-INF/web.xml
```xml
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE web-app
    PUBLIC "-//Sun Microsystems, Inc.//DTD Web Application 2.3//EN"
    "http://java.sun.com/dtd/web-app_2_3.dtd">
<web-app>
    <display-name>Hi There</display-name>
    <servlet>
        <servlet-name>sayhi</servlet-name>
        <servlet-class>com.example.packname.HelloServlet</servlet-class>
    </servlet>
    <servlet-mapping>
        <servlet-name>sayhi</servlet-name>
        <url-pattern>/there</url-pattern>
    </servlet-mapping>
</web-app>
```

##### Clean, prepare, and compile the project
    cd ~/git/tc-aws
    ant -v all
```
Apache Ant(TM) version 1.8.3 compiled on February 25 2015
Trying the default build file: build.xml
Buildfile: /home/bachmeb/git/tc-aws/build.xml
Detected Java version: 1.7 in: /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.91.x86_64/jre
Detected OS: Linux
parsing buildfile /home/bachmeb/git/tc-aws/build.xml with URI = file:/home/bachmeb/git/tc-aws/build.xml
Project base dir set to: /home/bachmeb/git/tc-aws
parsing buildfile jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml with URI = jar:file:/usr/share/java/ant.jar!/org/apache/tools/ant/antlib.xml from a zip file
 [property] Loading /home/bachmeb/git/tc-aws/build.properties
 [property] Unable to find property file: /home/bachmeb/git/tc-aws/build.properties
 [property] Loading /home/bachmeb/build.properties
Trying to override old definition of datatype resources
Build sequence for target(s) `all' is [clean, prepare, compile, all]
Complete build sequence is [clean, prepare, compile, all, reload, install, remove, list, javadoc, dist, ]

clean:

prepare:
    [mkdir] Created dir: /home/bachmeb/git/tc-aws/build
    [mkdir] Created dir: /home/bachmeb/git/tc-aws/build/WEB-INF
    [mkdir] Created dir: /home/bachmeb/git/tc-aws/build/WEB-INF/classes
     [copy] No sources found.
     [copy]  omitted as /home/bachmeb/git/tc-aws/build is up to date.
    [mkdir] Created dir: /home/bachmeb/git/tc-aws/build/WEB-INF/lib

compile:
    [mkdir] Skipping /home/bachmeb/git/tc-aws/build/WEB-INF/classes because it already exists.
    [javac] No sources found.
     [copy] No sources found.
     [copy]  omitted as /home/bachmeb/git/tc-aws/build/WEB-INF/classes is up to date.

all:

BUILD SUCCESSFUL
Total time: 0 seconds
```
##### Reinstall the project
    cd ~/git/tc-aws
    ls
    ant install

##### View the web app in Lynx
    lynx http://localhost:8080/hello
    
##### View the app in a web browser on your PC
	wget http://ipinfo.io/ip -qO -
	http://[ec2.ipa.ddr.ess]:8080/hello
