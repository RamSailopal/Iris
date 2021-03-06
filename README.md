Role Name
=========

This role automates the process of installing Intersystems IRIS on a Linux machine unattended.

Requirements
------------

It is assumed that Iris is to be installed on either a Red Hat or SuSE derived system as advised by Intersystems

It is also assumed that you have a Intersystems IRIS installation tar file which is deposited in the files directory. The name of this file then need to be set in the inst_tar variable (see below)


Role Variables
--------------

inst_tar - The name of the tar file that will be installed from

[ Default - IRIS_Community-2020.1.1.408.0-lnxrhx64.tar.gz ]

package - The architecture of the linux environment. Can be one of:

lnxrhx64 - Red Hat Enterprise Linux (x64) - 64 bit
lnxrhx86 - Red Hat Enterprise Linux (Intel) - 32 bit
lnxsusex64 - SuSE Linux Enterprise Server (x64) - 64 bit
lnxsusex86 - SuSE Linux Enterprise Server (Intel) - 32 bit

[ Default - lnxsusex86 ]

instname - The name of the Iris instance to install

[ Default - TEST ]

inst_dir - Where to install Iris

[ Default - /usr/local/iris ]

sec - The level of security to initially install with (either Minimal,Normal or Lockdown)

[ Default - Minimal ]

mangrp - The management group to run Iris under

[ Default - irisadmin ]

manusr - The management user to run Iris under

[ Default - irisadmin ]

mangrp - The management group to run Iris under

[ Default - irisadmin ]

irisusr - The normal user to run Iris under

[ Default - iris ]

irisgrp - The normal group to run Iris under

[ Default - iris ]

csppass - CSP System User Password

[ Default - Dummy ]

userpass - Password that is required for Normal or Lockdown Security modes. If Minimal is selected, this settingis ignored

[ Default - Dummy ]

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      role: iris
      platform: lnxrhx86
      instname: IRIS
      ...

License
-------

BSD

Author Information
------------------

Raman Sailopal
