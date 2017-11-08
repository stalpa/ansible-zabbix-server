role name : ansible-zabbix-server for Ubuntu instance 

playbook steps:
* Install release,dependencies
install_epel.yml
* Install apache2
install_httpd.yml
* Install and setup Percona DB
install_percona.yml
* Install and setup PHP
install_php.yml
* Install/Setup ZABBIX,
main.yml

Actions:
* Install release, .. [packages]
* Install httpd (start, enabled)
* Install/Setup Percona DB (start, enabled)
* Install/Setup PHP
* Download/Install Zabbix Repository
* Install Zabbix-Server
        zabbix-server-mysql
        zabbix-web-mysql
* Setting database (create DB, user)
* Setting zabbix_server.conf
* Start zabbix-server (enabled), Restart apache2
