# Learning-HAProxy
Simple HAProxy demo for learning. 

## What is this repo?

I am going over the process of learning [HAProxy](https://www.haproxy.org/) and figured it's a 
good idea to create a demo how this works by using [Vagrant](https://www.vagrantup.com) plus 
some other tools.

## How can I use this?

You will need the following before getting started. 

* Virtualbox - https://virtualbox.com
* Vagrant - https://vagrantup.com
* Git - https://git-scm.com/ (optional, you can download directly from Github)

Once you have those installed, you can continue to the next part. 

## Creating the lab

1) Clone or download this directory locally

2) Start the machines using the command ``$ vagrant up``

Note - this will take a few minutes to download the Ubuntu image.

3) Once the machines are completed, check the status using ``$ vagrant status``

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


