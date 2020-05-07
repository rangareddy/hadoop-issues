# hadoop-issues
Hadoop Component Related Issues and Solutions

1. Permission denied: user=root, access=WRITE, inode="/user":hdfs:supergroup

Solution: User **user** doesn't have a **write** permission. First login with **hdfs** user and create a directory for **user**.
```
sudo -u hdfs hadoop fs -mkdir /user/root
sudo -u hdfs hadoop fs -chown root /user/root
```
