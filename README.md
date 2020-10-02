# hadoop-issues

## 1. AccessControlException: Permission denied: user=root, access=WRITE, inode="/user/root/.staging":hdfs:hdfs:drwxr-xr-x

**Solution:** User **user** doesn't have a **write** permission. First login with **hdfs** user and create a directory for **user**.
```shell
sudo -u hdfs hadoop fs -mkdir /user/root
sudo -u hdfs hadoop fs -chown root /user/root
```

## 2. Spark-shell is not working in HDP 2.6.5 version

**Solution:** 
```shell
# export SPARK_MAJOR_VERSION=2 
# spark-submit --version
SPARK_MAJOR_VERSION is set to 2, using Spark2
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.3.0.2.6.5.0-292
      /_/
                        
Using Scala version 2.11.8, Java HotSpot(TM) 64-Bit Server VM, 1.8.0_112
Branch HEAD
Compiled by user jenkins on 2018-05-11T08:28:14Z
Revision b6b578c8dff89bfc07981ea3bda074262c3800ad
Url git@github.com:hortonworks/spark2.git
```

