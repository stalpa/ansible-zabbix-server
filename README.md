# zabbix-v3-on-Centos-v6

role name : zabbix_install

playbook steps:
* Install epel (fpint,iksemel)
install_epel.yml
* Install httpd
install_httpd.yml
* Install and setting Mariadb
install_mariadb.yml
* Install and setting php (set php timezone)
install_php.yml
* Include, Download/Install ZABBIX,
* Setting database
main.yml

Actions:
* Install epel-release, fpint, iksemel
* Install httpd (start, enabled)
* Install and setting Mariadb (start, enabled)
* Install and setting PHP, set php.timezone
* Download/Install Zabbix Repository
* Get/Import RPM-GPG-KEY-ZABBIX
* Install Zabbix-Server
        zabbix-server-mysql
        zabbix-web-mysql
        zabbix-agent
        zabbix-get
* Setting database (create DB, user)
* Setting zabbix_server.conf
* Copy a new 'zabbix.conf.php' file into place
* Start zabbix-server (enabled), Restart httpd

Info Needed:
* CentOS 7.2
* Zabbix 3.0

P.S.
#don't forget disable firewall
systemctl stop firewalld && systemctl disable firewalld

Documentation:
https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages
http://www.server-world.info/en/note?os=CentOS_7&p=zabbix30

