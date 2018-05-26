# ansible-gce-apache-lb
=========

Playbooks to create simple instances of gce centos/apache with load balancing

Requirements
------------

+ Steps described in [Google Cloud Platform Guide](http://docs.ansible.com/ansible/latest/scenario_guides/guide_gce.html)

Variables
--------------

You need to modify the playbooks with the corresponding variables of your GCP account:

```
  vars:
    service_account_email: *[Your gce service account email]*
    credentials_file: *[Your json credentials file]*
    project_id: *[Your project id]*


    metadata: '{"sshKeys":"*[Your gce user: Your rsa public key]*"}'

    remote_user: *[Your gce user]*

```

Dependencies
------------

These playbooks were successfully tested in Fedora 26 and CentOS 7 with Ansible 2.5.

Example Playbook Run
----------------

You need to run the playbook specifying the private key file to connect to the gce instances:

```
$ ansible-playbook gce-lb-apache.yml --key-file *[Your rsa private key path]*
```

License
-------

BSD

Author Information
------------------

This playbooks was created in 2018 by [Alex Callejas](https://www.twitter.com/dark_axl), blog [rootzilopochtli.com](https://www.rootzilopochtli.com/).
