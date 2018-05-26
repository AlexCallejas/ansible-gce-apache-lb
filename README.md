# ansible-gce-apache-lb

Playbooks to create simple instances of gce centos/apache with load balancing

Requirements
------------

+ Steps described in [Google Cloud Platform Guide](http://docs.ansible.com/ansible/latest/scenario_guides/guide_gce.html)

Variables
--------------

You need to modify the playbooks with the corresponding variables of your GCP account:

```
  vars:
    service_account_email: _Your gce service account email_
    credentials_file: _Your json credentials file_
    project_id: _Your project id_


    metadata: '{"sshKeys":" _Your gce user: Your rsa public key_ "}'

    remote_user: _Your gce user_

```

Dependencies
------------

These playbooks were successfully tested in Fedora 26 and CentOS 7 with Ansible 2.5.

Example Playbook Run
----------------

You need to run the playbook specifying the private key file to connect to the gce instances:

```
$ ansible-playbook gce-lb-apache.yml --key-file _Your rsa private key path_
```

License
-------

BSD

Author Information
------------------

This playbooks was created in 2018 by [Alex Callejas](https://www.twitter.com/dark_axl), blog [rootzilopochtli.com](https://www.rootzilopochtli.com/).
