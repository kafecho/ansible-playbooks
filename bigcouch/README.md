bigcouch
========
Overview
--------
As the name suggests, this is a playbook for installing and configuring a [BigCouch](http://bigcouch.cloudant.com/) cluster using Ansible.
I essentially took the instructions from the [cloudant user guide](http://bigcouch.cloudant.com/use) and turned them into an actionable playbook. 

Target OS
---------
I implemented this playbook using Vagrant and VMs running CentOS 6.3 64 bit. 
As I use Vagrant with host_only networking, each vm ends up with two IP addresses.
For the moment, the playbook tasks are hard coded to use the 2nd IP address.

I am also using the nodes' IP addresses instead of their fully qualified hostnames. This setup is a bit simpler (no need for DNS or fiddling with /etc/hosts) and seems to work just as well.

How to use
----------
In order to use, modify the hosts file and add entries under the tag 'bigcouchservers'

Stuff to do
-----------
This is work in progress. 

Changelog
---------
01/08/2013: refactored according to Ansible best practices (added a dedicated role for bigcouch).
31/07/2013: initial version commit




