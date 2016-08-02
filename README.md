# ansible-zabbix3.0-centos7
Install Zabbix Server3.0 on CentOS7

#Requirements
Ansible 1.4 or higher and platform.

#System Requirements
CentOS7.x Minimal Install

#How to install
 (1) sudo yum install -y git epel-release<br>
 
 (2) sudo yum makecache<br>
 
 (3) sudo yum install -y ansible git<br>
 
 (4) sudo git clone [GitHub URL]<br>
 
 (5) cd ansible-zabbix3.0-centos7<br>
 
 (6) vi group_vars/zabbix-server-mariadb-standalone<br>
 ------<br>
 # Set DB Password<br>
 DBPassword: <password> ← DBパスワードの設定<br>
 ------<br>
 
 (7) Ansoble　playbookを利用してZabbix3.0のインストールを開始<br>
   sudo ansible-playbook -i hosts install.yml<br>
 
 (8) インストール後Firewallを停止<br>
   systemctl stop firewalld<br>
 
 (9) ZabbixのURLに接続<br>
 http://<SERVER IP Address>/zabbix/
