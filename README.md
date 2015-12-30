ansible-role-sssd
=========

Configures a Linux server to use sssd and LDAP for system authentication.

Tested on EL6 and EL7

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
 - ldap\_password - this variable needs to have the password of the bind-account.

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
