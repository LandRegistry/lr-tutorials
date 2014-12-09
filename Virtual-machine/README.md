#Virtual machine

This directory contains a Vagrantfile basic virtual machine (or vm).
To start and use the virtual machine, see the quick reference guide below.

##how to make your own.

There are great instructions on virtual machines here on the vagrant website:

###https://docs.vagrantup.com/v2/

The website explains in more detail what we're doing below - but with different settings.

###Install vagrant: https://docs.vagrantup.com/v2/installation/
###And install virtualbox: https://www.virtualbox.org/  

##Project setup

The vagrant documentation explains this very well.  The instructions below detail how to 
setup vagrant to run the Basic Flask App.  If you haven't see the basic flask app - go here:

https://github.com/LandRegistry/lr-tutorials/tree/master/Basic-Flask-App

Check that your current working directory is lr-tutorials, then run the following command:

```shell
vagrant init
```

Which will create a Vagrantfile. This file marks the root directory of your project and describes
the kind of machine and resources you need to run your project, as well as what software to install 
and how you want to access it.

###Add a box
Which means telling vagrant what kind of virtual machine you want.  You can download many different
kinds of boxes, like Ubuntu and CentOS flavours of linux.  But we are going to use a Land Registry 
ubuntu image.

Update Vagrantfile so that this part:

 
```shell
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
```

```shell
config.vm.box = "base"
```

looks like this:

```shell
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
```

```shell
config.vm.box = "ubuntu/trusty64"
```

You will be able to start, access and stop the vm now.  See the quick reference guide below.

###Synced folders
The virtual machine and your PC can share files .  So if you type this in your vm:

```shell
ls /vagrant
```

Then you will see the contents of lr-tutorials. If you make changes to the contents of 
lr-tutorials, the changes will be reflected in the vagrant folder of your vm.  And visa versa.

###Provsioning the virtual machine
Do this to automate tasks.  For instance the basic flask app needs flask installed.  the provisioning script
can do this automatically.  Create a new file called provision.sh alongside your Vagrantfile.  Put this in it:

```shell
#!/usr/bin/env bash
```

```shell
pip install flask
```

The first line is a 'shebang' that says "run in the bash shell".  The next line tells pip 
(a python package manager) to install flask.  

Next tell vagrant to run the provision script by changing adding this line to the Vagrantfile:

```shell
config.vm.provision :shell, path: "provision.sh"
```

It goes under the line that says get the Land Registry Ubuntu image.

###Port Forwarding
You can run the basic flask app in the vm now.  But you can't view the running app in a browser on
your host pc.  For that you need to forward the port.

Add this to the Vagrantfile:

```shell
config.vm.network "forwarded_port", guest: 5000, host: 5000
```

There is a port forwarding section in the Vagrantfile you can use, or you can add it below the line you
added before.


##quick reference:

To start a vm:

```shell
vagrant up
```

To use a VM:

```shell
vagrant ssh
```

To stop a virtual machine

```shell
vagrant halt
```

To destroy a virtual machine.  For those times when its just easier to start again.

```shell
vagrant destroy
```

To reload a Vagrantfile

```shell
vagrant reload
```


