macklus.php
===========

General role for manage PHP versions, repository and configurations.


Install
-------

Install using command:
```bash
ansible-galaxy install macklus.php
```


Role Variables
--------------

macklus:
  php:
    ondrej:
      repository: true
      install: true
      versions: 
        absent: [ ]
        present: [ 5.6, 7.0, 7.1, 7.2, 7.3 ]

* **macklus.php.ondrej.repository:** Install Ondrej ppa (true|false)
* **macklus.php.ondrej.install:** Install packages from macklus.php.ondrej.versions (true|false)
* **macklus.php.ondrej.versions.absent:** PHP versions that should **not** be installed
* **macklus.php.ondrej.versions.present:** PHP versions to install


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
        remote_user: root
        roles:
          - macklus.php/ondrej/repository
          - macklus.php/ondrej/install


License
-------

GPL-3.0-only