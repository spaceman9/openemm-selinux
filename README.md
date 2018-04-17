# OpenEMM SELinux Module
This is an SELinux module for OpenEMM

Centos uses SELinux, which can cause some runtime issues with OpenEMM

This is a module that allows allows OpenEMM to work correctly without disabling SELinux.

This is currently working with OpenEMM 2015 R3, using Centos 6.9

A Longer explanation of how and why can be found here:
https://malacandra.blogspot.co.uk/2012/06/openemm-with-selinux.html

## Quick Install

First make sure the /home/openemm security context is correct. (use ls -Z to check).

`# restorecon -r /home/openemm`

`# yum install policycoreutils-python`

Go to the downloaded policy file and compile it.

`# ./make_policy openemm`

`# semodule -i openemm.pp`

