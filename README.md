role name : ansible-zabbix-server

playbook steps:
* Install epel-release,dependencies
install_epel.yml
* Install httpd
install_httpd.yml
* Install and setup Percona DB
install_percona.yml
* Install and setup PHP
install_php.yml
* Install/Setup ZABBIX,
main.yml

Actions:
* Install epel-release, .. [packages]
* Install httpd (start, enabled)
* Install/Setup Percona DB (start, enabled)
* Install/Setup PHP
* Download/Install Zabbix Repository
* Get/Import RPM-GPG-KEY-ZABBIX
* Install Zabbix-Server
        zabbix-server-mysql
        zabbix-web-mysql
        zabbix-agent
        zabbix-get
* Setting database (create DB, user)
* Setting zabbix_server.conf
#* Copy 'zabbix.conf.php' file into the place '/etc/zabbix/web'
* Start zabbix-server (enabled), Restart httpd
