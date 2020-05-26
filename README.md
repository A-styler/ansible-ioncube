Ioncube
=========
[![Build Status](https://travis-ci.org/cristian04/ansible-ioncube.svg?branch=master)](https://travis-ci.org/cristian04/ansible-ioncube)

This role will download  the [Ioncube loaders 64Bits](http://www.ioncube.com/loaders.php) into a specified folder.

By default, it will decompress the package into `/opt` but it can be changed using the ioncube_path variable.

Role Variables
--------------
`php_ioncube_path: /opt` Folder where you want to install ioncube
`php_ioncube_version: 10.3.9` Version of ionCube
`php_version: 7.3` Version of your PHP


Example Playbook
----------------

    ---
    - name: Install ioncube
      hosts: all
      become: yes
      vars:
        php_ioncube_path: "/opt"
        php_ioncube_version: "10.3.9"
        php_version: "7.3"
      roles:
        - ansible-ioncube
