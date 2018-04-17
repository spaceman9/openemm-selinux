# openemm-selinux
Selinux module for OpenEMM

Centos uses SELinux, which can cause some runtime issues with OpenEMM

This is a module that allows allows OpenEMM to work correctly without disabling SELinux.

This is currently working with OpenEMM 2015 R3, using Centos 6.9

A Longer explanation of how and why can be found here:
https://malacandra.blogspot.co.uk/2012/06/openemm-with-selinux.html

## Quick Install

`\# yum install policycoreutils-python`

`\# ./make_policy openemm`

`\# semodule -u openemm.pp`

