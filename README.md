Role Name
=========

This role automates the process of installing Intersystems IRIS on a Linux machine unattended.

Requirements
------------

It is assumed that Iris is to be installed on either a Red Hat or SuSE derived system as advised by Intersystems

It is also assumed that you have a Intersystems IRIS installation tar file which is deposited in the files directory and called IRIS_Community-2020.1.1.408.0-lnxrhx64.tar.gz


Role Variables
--------------

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

mangrp - The management group to run Cache under

[ Default - irisusr ]

cspbool - Whether to install Cache Server Pages or not (Y or N)

[ Default - Y ]

servtyp - What type of web stack you are running (either Apache of Nginx)

[ Default - Apache ]

csp_dir - Where to install Cache Server Pages (CSP)

[ Default - /opt/cspgateway ]

key_bool - Whether you have a Cache key/licence file to copy (Y or N) If Y then you must pass the variable key_loc which should contain the location of the key file on the local server

[ Default - N ]

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
