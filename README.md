# keti_trend_senario

0. install the libraries and packages

1. Downloads and install zip files from  (http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html)
 * instantclient-basic
 * instantclient-sdk

2. Set the environment variables on ~/.bashrc or /etc/profile:
"'
     export ORACLE_HOME=/path/your/files/instantclient_11_2
     export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$ORACLE_HOME
"'

3. make link files:
 '''
 cd $ORACLE_HOME
 ln -s libclntsh.so.11.1   libclntsh.so
 ln -s libocci.so.11.1   libocci.so
 '''

4. Edit oracle.conf file:
 '''
 echo $ORACLE_HOME > /etc/ld.so.conf.d/oracle.conf
 sudo ldconfig
 '''

5. Install cx_Oracle module:
 '''
 sudo easy_install cx_Oracle
 '''

6. Install InfluxDB:
 '''
 wget https://dl.influxdata.com/influxdb/releases/influxdb_1.1.1_amd64.deb
 sudo dpkg -i influxdb_1.1.1_amd64.deb
 '''
