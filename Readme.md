About
-----

Ansible role for installing Sikulix on a host.
At beginning it only supports Linux (RedHat compatible systems) and macos.


Role Variables
--------------

Variables with examples / defaults:

```yml
# URL to download installation archive from
sikuli_jar_url: "https://launchpad.net/sikuli/sikulix/1.1.1/+download/sikulixsetup-1.1.1.jar"
# checksum (md5) for this file
sikuli_jar_md5: "d48c93dac5cf6149fd81e694ef4e4011"

# location the install setup file should be downloaded to
# on linux this is also the location where the installed file are kept
sikuli_jar_dl_location: "/usr/etc/sikuli/sikulixsetup.jar"

# default options for unattended setup
sikuli_installopts: "options 1.1 buildv notes"

## Mac specific Variable:
# The folder the .app file and binary 'runsikulix' should be installed to
sikuli_jar_dl_location_mac: "/Applications/Sikulix/sikulixsetup.jar"
```


Usage
-----
 Example playbook:
```yml
- hosts:
    - localhost
  roles:
  - sikulix
```


Requirements
------------

Sikulix requires
* an X11 environment on Linux to run Sikulix afterwards (not needed for install).
* a Java runtime environment installed - preferably from Oracle.

This is not checked for by this role!


Acknowledgements
----------------

* thanks to https://github.com/RaiMan/SikuliX-2014/issues/69
* thanks to https://launchpadlibrarian.net/181066204/sikuli_install.sh


See also
--------

https://sikulix-2014.readthedocs.io/en/latest/faq/010-command-line.html


License
-------

MIT
