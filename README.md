# zabbix-repo


This roles manages official zabbix repositories from the **repo.zabbix.com**

To offload the traffic, the role is caching the downloaded packages in the `zabbix_repo_cache_dir ` directory. The workflow is

- download the package from the **repo.zabbix.com** if not already done
- copy the package to the remote hosts
- install the package

## Requirements

- ansible: 2.1


## Role Variables

`zabbix_repo_version` the version of package to be installed. default value is `null`, which means the recommended version from the **OS specific var file**  will be installed, mostly the latest LTS.

`zabbix_repo_tmp_dir` is the directory, where the **zabbx-repo** package will be saved on managed host defaults to **/tmp**.

`zabbix_repo_cache_dir` is the directory, where the role will cache the **zabbix-repo** package on local server, defaults to **/tmp**. I use **{{playbook_dir}}/files/zabbix/packages**.


## Dependencies

None

## Example Playbook

    - hosts: all
      roles:
         - hudecof.zabbix_repo

## License

BSD

## Author Information

Peter Hudec
