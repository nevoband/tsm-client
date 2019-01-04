Role Name
=========

Not full functionaly version of TSM client install for UIC tivoli storage manager

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Example: 

````yml
#password for initial install
tsm_client_password: "{{ vault_tsm_client_password }}"
````
Optional variables with defaults
````yml
#node information for TSM
tsm_client_server_name: "UIC_ADSM"
tsm_client_tcp_port: "1500"
tsm_client_server_address: "{{ ansible_nodename }}.adsmserv.uic.edu"
tsm_client_node_name: "{{ ansible_nodename }}"
tsm_client_password: ""

#Where to put the configs
tsm_client_opt_path: "/opt/tivoli/tsm/client/ba/bin"

#installation files and temporary directory to extract to
tsm_client_packages_tar: "https://accc.webhost.uic.edu/assets/files/adsm_backup/linux/v7.1/latest/7.1.6.5-TIV-TSMBAC-LinuxX86.tar"
tsm_client_package_dest: "/tmp"

#Logs location
tsm_client_error_log: "/var/log/tsm/dsmerror.log"
tsm_client_sched_log: "/var/log/tsm/dsmsched.log"
````


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: tsm-client }

License
-------

BSD
