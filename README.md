[![Build Status](https://travis-ci.org/CSCfi/ansible-role-sssd.svg?branch=master)](https://travis-ci.org/CSCfi/ansible-role-sssd)

ansible-role-sssd
=========

Configures a Linux server to use sssd and LDAP for system authentication.

Tested on EL6, EL7, Gentoo, Arch and Ubuntu

 - CI testing of EL6/EL7 and Ubuntu.

copy templates/sssd-example.conf.j2 to templates/sssd.conf.j2 and modify it
 - sssd.conf.j2 is ignored from git

Requirements
------------

 - Certificate needs to be from TERENA (so _probably_ others or TERENA3 does not work)
  - This should be configurable. PRs are welcome.

Role Variables
--------------

By default nothing is done by this role because:
<pre>
sssd_configure: False
</pre>

Set it to True to configure sssd.

See:
 - defaults/main.yml and vars/main.yml
 - templates/sssd-example.conf.j2
 - templates/sssd.conf.gentoo.j2 (also for Ubuntu & Arch)

<pre>
ldap_password: "ldap_bind_password"
</pre>

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-sssd, sssd_configure=True }

License
-------

MIT

Author Information
------------------

Originally written by Marco Passerini https://github.com/mpasserini . Moved into public Github by Johan Guldmyr @ CSC
