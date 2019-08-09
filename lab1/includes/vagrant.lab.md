<section id="vagrant_lab" class="section">

## Lab Prep

To follow along, you'll need the following:

1. [vagrant](https://www.vagrantup.com/downloads.html)
1. [virtualbox](https://www.virtualbox.org/)

Again, some notes:

- The <a href="#" class="flash" data-selector="#requirements" data-duration="300">Install Lab Requirements</a> button above is experimental and may not work, but you can give it a try (only if you're on Windows).<br />
  You'll be presented with an installation menu from which you can choose to install vagrant, among other tools.
- **All** of my testing is being done from a [cmder](http://cmder.net/) bash terminal, so if you want to follow along, I suggest you install that tool.

Once you've met all requirements, we can proceed in preparing your local lab environment.

Moving along ☞

## Initializing virtual machines using vagrant

1. Again, you'll need the **vagrant** command installed to follow along, so make sure you've obtained the requisite programs.
1. From your terminal, create a new directory under ~/git/vagrant:
	- `mkdir -p ~/git/vagrant`
	- `cd ~/git/vagrant`
1. Initialize a vagrant project based on the Ubuntu Xenial x64 box (a.k.a. VM Template)
	- `vagrant init -m ubuntu/xenial64`<br />
	The vagrant command will notify you once it's done<br />
	It will have created a file named *Vagrantfile* in the current directory<br />
	This is the file that *defines* your Virtual Machine (VM)
1. Review the status of the virtual machine 
	- `vagrant status`<br />You should see something similar to:<br /><br />![vagrant status](!ifdef(assets_folder)(!assets_folder)(!cwd/../assets)/images/vagrant_status.gif)
1. Now that you are aware of the available machines, let's boot up the **!vagrant_machine** host:
	- `vagrant up !vagrant_machine`<br />You should see something similar to:<br /><br />![vagrant up](!ifdef(assets_folder)(!assets_folder)(!cwd/../assets)/images/vagrant_up.gif)
1. You'll observe that vagrant takes the following actions:
	- Checks for the **machine** **box** as specified in the **Vagrantfile**
	- Downloads the **box** locally if necessary<br />i.e., if the box has already been downloaded, vagrant will happily use the cached version
	- Boots up the **machine** using the **box** image
	- Checks if the initial **provisioning** tasks have been run against the **machine**,<br /> and if not, will run the initial provisionment task(s)
1. Again, vagrant is simply 'talking' to the underlying hypervisor and cycling through several phases of the machine boot up process, as illustrated:<br /><br />![Vagrant 'talking' to Virtualbox](!ifdef(assets_folder)(!assets_folder)(!cwd/../assets)/images/vagrant_up_diagram.png)
1. If you launch Virtual Box, you'll see your Virtual Machine in the list of VMs:<br />![Virtual Box](!ifdef(assets_folder)(!assets_folder)(!cwd/../assets)/images/virtualbox.png)

## Accessing your machines using vagrant

The machine *!vagrant_machine* should be booted and ready for action 😎

You can now `ssh` into the machine and play around the terminal:<br />

`vagrant ssh !vagrant_machine`

I encourage you to read through the [vagrant documentation](https://www.vagrantup.com/docs/) for in-depth information.

## This concludes lab1. 

In lab2, we'll be creating a Windows-Based Virtual Machine!

Lab2 will cover:

- Creating Windows-Based Vagrant Boxes using [packer](https://www.packer.io/intro/getting-started/vagrant.html)
- Bootstrapping the Windows VM using the [vagrant provision](https://www.vagrantup.com/docs/cli/provision.html) command
- Interacting with your Windows VM

</section>