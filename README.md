# keti_trend_senario

0. install the libraries and packages

1. Downloads and install zip files from  (http://www.oracle.com/technetwork/database/features/instant-client/index-097480.html)
 * instantclient-basic
 * instantclient-sdk

2. Set the environment variables on ~/.bashrc or /etc/profile:
<pre><code>export ORACLE_HOME=/path/your/files/instantclient_11_2
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$ORACLE_HOME
</code></pre>

3. make link files:
<pre><code>cd $ORACLE_HOME
 ln -s libclntsh.so.11.1   libclntsh.so
 ln -s libocci.so.11.1   libocci.so
</code></pre>

4. Edit oracle.conf file:
<pre><code>echo $ORACLE_HOME > /etc/ld.so.conf.d/oracle.conf
 sudo ldconfig
</code></pre>

5. Install cx_Oracle module:
<pre><code>sudo easy_install cx_Oracle
</code></pre>

6. Install InfluxDB:
<pre><code>wget https://dl.influxdata.com/influxdb/releases/influxdb_1.1.1_amd64.deb
 sudo dpkg -i influxdb_1.1.1_amd64.deb
 sudo pip install influxdb
 </code></pre>
