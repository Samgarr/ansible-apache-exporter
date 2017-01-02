Role Name
=========

Built and run [Apache Exporter](https://github.com/neezgee/apache_exporter) for [Prometheus](https://prometheus.io). Roughly tested in production environment.
Pull requests are welcomed.

Requirements
------------

* Working GO environment. I'm going with Joshua Lund's [ansible-go](https://github.com/jlund/ansible-go) role.
* Prometheus, this role is tested with William Yeh's [ansible-prometheus](https://github.com/William-Yeh/ansible-prometheus).


Role Variables
--------------

Please see [defaults/mail.yml](defaults/mail.yml) and [tasks/set-role-variables.yml](tasks/set-role-variables.yml).


Example Playbook
----------------


    - hosts: servers
      vars:
        apache_exporter_goroot: /usr/local/go
        apache_exporter_gopath: /tmp/apache_exporter_work/gopath
        prometheus_components:
          - apache_exporter
      roles:
         - { role: ansible-apache-exporter }

License
-------

The MIT License (MIT)

Author Information
------------------

Feel free to contact me [here on Github](https://github.com/Samgarr).
