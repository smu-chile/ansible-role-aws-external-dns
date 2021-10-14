Role Name
=========

Role to create a sealed secret deployment on a kubernetes cluster



Role Variables
--------------

```
      AWS_ACCESS_KEY_ID
      AWS_SECRET_ACCESS_KEY
      REGION: AWS region
      CLUSTER_NAME
      ROOT_DOMAIN
```

Example Playbook
----------------


```
- hosts: "{{ lookup('env','BASTION_IP') }}"
  become: no
  remote_user: "ubuntu"
    - role: external-dns
      AWS_ACCESS_KEY_ID: "{{ lookup('env', 'AWS_ACCESS_KEY_ID') }}"
      AWS_SECRET_ACCESS_KEY: "{{ lookup('env', 'AWS_SECRET_ACCESS_KEY') }}"
      REGION: "{{ lookup('env', 'REGION') }}"
      CLUSTER_NAME: "{{ lookup('env', 'CLUSTER_NAME') }}"
      ROOT_DOMAIN: "{{ lookup('env', 'ROOT_DOMAIN') }}"
```

License
-------

BSD

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)