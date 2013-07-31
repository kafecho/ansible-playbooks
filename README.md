ansible-playbooks
=================
My (hopefully growing) collection of playbooks for [Ansible](http://www.ansibleworks.com/)
bigcouch
--------
As the name suggests, this is a playbook for installing and configuring a [BigCouch](http://bigcouch.cloudant.com/) cluster using Ansible.
I essentially took the instructions from the [cloudant user guide](http://bigcouch.cloudant.com/use) and turned them into an actionable playbook. 

I implemented this playbook using Vagrant and VMs running CentOS 6.3 64 bit. 

As I use Vagrant with host_only networking, each vm ends up with two IP addresses. For the moment, the playbook tasks are hard coded to use the 2nd IP address.

I am also using the nodes' IP addresses instead of their fully qualified hostnames. This setup is a bit simpler (no need for DNS or fiddling with /etc/hosts) and seems to work just as well.

In order to use, simply add hosts to your inventory file under the tag 'bigcouchservers'

This is work in progress, and I need to tidy the code a bit to be more in line with Ansible best practices. 




