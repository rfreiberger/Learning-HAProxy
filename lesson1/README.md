## Lesson 1

This lesson is a very simple deployment of HAProxy and two
web servers. This is a example of HAProxy at it's most basic.

## Creating the lab

1) Clone or download this directory locally

2) Start the machines using the command ``$ vagrant up``

Note - this will take a few minutes to download the Ubuntu image.

3) Once the machines are completed, check the status using ``$ vagrant status``, you should see "running" on all machines.

```
$ vagrant status
Current machine states:

haproxyserver             running (virtualbox)
web1                      running (virtualbox)
web2                      running (virtualbox)

This environment represents multiple VMs. The VMs are all listed
above with their current state. For more information about a specific
VM, run `vagrant status NAME`.
```

4) To login to each machine, you can use the command ``$ vagrant ssh <vm name>``, example below

```
$ vagrant ssh haproxyserver
Welcome to Ubuntu 16.04.4 LTS (GNU/Linux 4.4.0-119-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

9 packages can be updated.
4 updates are security updates.


Last login: Tue May  1 21:32:21 2018 from 10.0.2.2
```

5) You can test HAProxy now

Open your browser to the following address http://10.0.0.100:8080 and you should
see the Web1 or Web2 hosts. Try refreshing to see this switch.

6) Once you are done, you can destroy the machines using the following command.

``$ vagrant destroy``

7) Done! 
