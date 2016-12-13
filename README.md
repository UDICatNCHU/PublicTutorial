# HadoopTutorial

我所建置的Hadoop機器：
  http://140.120.16.94:50030/jobtracker.jsp

登入方式：
ssh hduser@140.120.16.94 -p 16222

Account: _hduser_

Password: _hadoop_

## 關於帳號的創建

sudo adduser --ingroup hadoop **你的帳號**

例如：

``` 
sudo adduser --ingroup hadoop yao-chung 
```

## 修改hdfs 權限

```
cd /usr/local/hadoop/
bin/hadoop fs -chmod -R 777 /app/hadoop/tmp
bin/hadoop  fs -mkdir /user/你的帳號/
bin/hadoop fs -chown -R 你的帳號:hadoop /user/你的帳號/
```

## 使用自己帳號登入後，輸入下列設定檔
```
exit
ssh 你的帳號@140.120.16.94 -p 16222
```
### 登入後設定環境變數檔 (.bashrc)
```
export HADOOP_HOME=/usr/local/hadoop
export HADOOP_HOME=/usr/local/hadoop
```
### 登出後重新登入使設定檔生效 or 使用 source 指令
```
source .bashrc
```

# HDFS (Hadoop Distributed File System 基本操作):

1. 瀏覽HDFS內容
``` 
hadoop fs -l 
```

2. 創建目錄夾於HDFS中
```
hadoop fs -mkdir 目錄夾名稱
```

3. 存放資料於HDFS中
```
hadoop fs -put local_file_name hdfs_file_name
```

4. 從HDFS刪除資料
```
hadoop fs -rmr hdfs_file_name
```

5. 查看HDFS檔案內容
```
hadoop fs -cat file_name
```

6. 自HDFS中，取回檔案至本地端
```
hadoop fs -get hdfs_file_name local_file_name
```







