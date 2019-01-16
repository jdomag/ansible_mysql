# ansible_mysql
## Description
Role to install mysql server on RedHat / Centos 7

## Usage
1) Edit "production_inventory" file and add destination host where you will install MySQL server. Add a host to one of created groups e.g. wro_dbservers.
   Alternatively you can edit /etc/hosts and add entry for wro_db01 there e.g.:

 192.168.1.1 wro_db01 

2) Run playbook for all hosts:

  ansible-playbook -i production_inventory site.yml -u your_username -k -K 

  OR run it for single host:

  ansible-playbook -i production_inventory site.yml -u your_username -k -K --limit your_new_db_host_you_added_to_production_inventory

## MySQL version
You can define and change the mysql version by editing variable 'mysql_ver' in a file 'roles/dbtier/defaults/main.yml'.

