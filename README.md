# ansible-zabbix
Ansible playbooks and roles dedicated to working with zabbix

# playbooks
**The zabbix-api needs to be installed on the zabbix server for any of the zabbix modules to function correctly "pip3 install zabbix-api"**
zabbix_maint_group.yml - This adds a maintenence schedule in zabbix for a host group.  This is great for preempting notifications when you are about to service affecting updates.
  - server_url: I have this set to use http and is referencing the default install folder of /zabbix, so adjust as needed.
  - zab_host: Has the hard coded IP of the zabbix server.  You could/should pass this on run or reference a FQDN.
  - maint_group: Is the Zabbix host group name that will be put in maintenance.  
  - gen1_user/password: Are the zabbix login creds.  In tower I create some custom credentails for generic username and password logins, which is what you see here.  I pass these in at runtime.
  
