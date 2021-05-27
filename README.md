# monitor_portal_template
4us monitör portal
~~~
wget -qO- https://repos.influxdata.com/influxdb.key | gpg --dearmor > /etc/apt/trusted.gpg.d/influxdb.gpg
export DISTRIB_ID=$(lsb_release -si); export DISTRIB_CODENAME=$(lsb_release -sc)
echo "deb [signed-by=/etc/apt/trusted.gpg.d/influxdb.gpg] https://repos.influxdata.com/${DISTRIB_ID,,} ${DISTRIB_CODENAME} stable" > /etc/apt/sources.list.d/influxdb.list

~~~

~~~
sudo apt-get update && sudo apt-get install influxdb
sudo service influxdb start
~~~

~~~
sudo apt install telegraf
~~~
~~~
$ influx

> create database telegraf
> create user “telegraf” with password ‘P@ssword!’ with all privileges
> exit

Create Read-only user on Vsphere

nano /etc/telegraf/telegraf.conf

edit
[outputs.telegraf]
  no commit url
  username password
  
  
  [inputs.vsphere]
  
  change url and auth
  
  insecure_skip_verify = true


