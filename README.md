Role Name
=========

An Ansible role that installs maven on Ubuntu.

Requirements
------------

JDK should be installed before this role. You can include [openjdk role](https://galaxy.ansible.com/siavashoutadi/openjdk/) to install the JDK prior to maven.

Role Variables
--------------

```ansible
maven_version: 3.5.2
```

The version of maven to be installed.

```ansible
maven_destination_directory: /opt
```

Maven will be installed under this directory.

```ansible
maven_bin_url: http://apache.mirrors.spacedump.net/maven/maven-3/{{ maven_version }}/binaries/apache-maven-{{ maven_version }}-bin.tar.gz
```

The url for downling the maven binary file.

```ansible
maven_enable_bash_completion: true
```

A flag to indicate if the bash completion should be installed.

Dependencies
------------

N/A

Example Playbook
----------------

```ansible
- name: Install maven
  hosts: localhost
  become: true
  roles:
    - maven
```

License
-------

Apache
