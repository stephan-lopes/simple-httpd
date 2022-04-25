Simple Apache2/Httpd Server
=========

A simple httpd server.

Requirements
------------

  * Python 2.7
  * Ubuntu 20.04
  * Ansible >= 2.9

Role Variables
--------------
We have only one variable in the function, and it is set to install or remove HTTPD/Apache2.

```yaml
httpd_state: present # or absent
```

Dependencies
------------

N/A

Example Playbook
----------------

Below are some installation and removal examples:

### Install HTTPD

An example of installation would be the one below, using the httpd_state variable. If it is not informed, the default value is present.

``` yaml
- hosts: servers
  roles:
      - role: stephan_lopes.simple-httpd
        vars: 
        - httpd_state: present
```

### Remove HTTPD

To remove, set the absent value in the httpd_state variable.

``` yaml
- hosts: servers
  roles:
      - role: stephan_lopes.simple-httpd
        vars: 
        - httpd_state: absent
```
