# HadoopTutorial

我所建置的Hadoop機器：
  http://140.120.16.94:50030/jobtracker.jsp

登入方式：
ssh hduser@140.120.16.94 -p 16222

Account: _hduser_

Password: _hadoop_

# 關於帳號的創建

sudo adduser --ingroup hadoop **你的帳號**

例如：

``` 
sudo adduser --ingroup hadoop yao-chung 
```

# 修改hdfs 權限

```
cd /usr/local/hadoop/
bin/hadoop fs -chmod -R 777 /app/hadoop/tmp
bin/hadoop  fs -mkdir /user/你的帳號/
bin/hadoop fs -chown -R 你的帳號:hadoop /user/你的帳號/
```

# 使用自己帳號登入後，輸入下列設定檔
```
exit
ssh 你的帳號@140.120.16.94 -p 16222
```
## 登入後設定環境變數檔 (.bashrc)
```
export HADOOP_HOME=/usr/local/hadoop
export HADOOP_HOME=/usr/local/hadoop
```
## 登出後重新登入使設定檔生效 or 使用 source 指令
```
source .bashrc
```
