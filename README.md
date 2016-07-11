zabbix-repo for Ansible Based on hudecof/ansible_zabbix-repo

Supported dists:
--
EL 5-7

Debian 6-8

Ubundu 10.x - 14.x



Supported Versions:
--
2.0 - 3.0


=========
[11.06.2016] - Added Zabbix 3.0 Support

Installation of the official zabbix repozitories from http://repo.zabbix.com

Requirements
------------

[sudo] ansible-galaxy install Burnfaker.zabbix-repo

Role Variables
--------------

`zabbix_repo_recommend` is the list of the recommened version of the zabbix-repo package for each supported distribution. Feel free to ovveride it.

If for some reason you need to have diffent version installed on some **host** or **host_group** set `zabbix_repo_version`,

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - Burnfaker.zabbix-repo
		 
License
-------

BSD

Author Information
------------------

Peter Hudec
CNC, a.s.
