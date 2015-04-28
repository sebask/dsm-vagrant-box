# DSM Vagrant Box
A Vagrant box to get a virtualized Synology Diskstation Manager up and running. Based on XPEnology.

What you'll get:

* Virtualized DSM 5.1 (DSM 5.1-5022)
* Preconfigured Vagrant user
* Preconfigured Volume
* Preconfigured Package Center with SynoCommunity repo
* Vim

## How To

### Getting Started
You'll need the following applications on your machine:

- Vagrant (https://www.vagrantup.com)
- VirtualBox (https://www.virtualbox.org)

Open `Terminal.app`, and change to the directory where your code resides and where the `Vagrantfile` and `XPEnoboot_DS3615xs_5.1-5022.3.iso` are located.

For example:

```bash
cd ~/Development/virtual-dsm-machine
```

Start the virtual machine.

```bash
vagrant up
```

Depending on your host machine and internet connection this can take some time.

While Vagrant is getting your machine up and running you will be asked which network adapter should be used. For example, if you're on Wi-Fi this is probaly option `1`.

Your machine is now running!

### Access to your box
Find out the IP of your guest machine. Go to http://find.synology.com to connect to the virtual Synology box, use the Synology Assistant (http://www.synology.com/en-us/support/download), or use something else.

### Some notes
This box is **only** prepped to make developing for DSM a little bit easier. Use it wisely.

DSM does not contain everything Vagrant expects. Stuff like `sudo` is missing and therefore commands like `vagrant halt` won't work out of the box.

### Thanks
Information from http://wijngaard.org helped me a lot while creating this box.
