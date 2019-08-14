<section id="vagrant_introduction" class="section">

## What is Vagrant?

* [Vagrant](https://www.vagrantup.com/) is an  open-source software product for building and 
maintaining portable virtual software development environments:
  * Aims to simplify configuration management of virtualizations in order to increase development productivity 
  * Written in the Ruby programming language, and is thus highly extensible
  * Supports numerous hypervisor [providers](https://www.vagrantup.com/docs/providers/), for example:
      - [VirtualBox](https://www.vagrantup.com/docs/virtualbox/)
      - [Hyper-V](https://www.vagrantup.com/docs/hyperv/)
      - [VMware](https://www.vagrantup.com/docs/vmware/)
      - [KVM/libvirt](https://github.com/vagrant-libvirt/vagrant-libvirt)
* It is a commandline tool
* Under the hood, it's just sending commands to the corresponding [hypervisor](https://www.reddit.com/r/explainlikeimfive/comments/l16v7/eli5_hypervisor/)

![Vagrant 'talking' to Virtualbox](lab1/assets/images/vagrant_up_diagram.png)

Think of it like this:

<span style="font-size: 1.5em">Vagrant</span> is to **Virtual Machines** what <span style="font-size: 1.5em">[Docker](https://www.reddit.com/r/sysadmin/comments/33uts6/eli5_docker_what_exactly_is_it_what_does_it_do/)</span> is to **Containers**

### Terminology

Throughout the sections ahead, I'll make reference to the following terms:

- [box](https://www.vagrantup.com/docs/boxes.html) - This is vagrant terminology for *base image*
A box is similar to a **.vmdk** file in **vmware**<br />
In fact, you can convert a **.vmdk** file to vagrant **.box** format using [qemu-img convert](https://docs.openstack.org/image-guide/convert-images.html)<br />
The process is rather involved, and is essentially a conversion from **.vmdk** => **.qcow2** => **.box**
- **machine**: [Virtual machine](https://www.reddit.com/r/explainlikeimfive/comments/1a86vh/eli5_what_is_a_virtual_machine_how_does_it_work/)

### Installation

I've provided a means of installing **all** the requirements for this lab.

Just click the <a href="#" class="flash" data-selector="#requirements" data-duration="300">Install Lab Requirements</a> button above.

It's rather experimental and may not work, but you can give it a try (again, only if you're on Windows).<br />

You'll be presented with an installation page from which you can choose to install everything you need.

If that doesn't work, you can opt to install vagrant **manually**, as follows:

1. Navigate to the vagrant downloads site: [vagrant downloads](https://www.vagrantup.com/downloads.html)
1. Once downloaded, launch the installer and follow the prompts
  - The installer will make the `vagrant` command available to your command-line terminal via your *PATH* variable
  - If upon installation, the `vagrant` command is not found, you may need to restart whatever terminal you have open, e.g. cmd, bash, iterm2, cygwin, etc

I **highly** recommend you install the following applications along with **vagrant**:
  - [cmder](http://cmder.net/)<br />
    The commandline experience presented through it more closely matches a posix-compliant operating environment
  - [Sublime Text 3](https://www.sublimetext.com/3)<br />
    Forget Notepad++, just throw it away. This one is king!

Once you've installed the tools, proceed to the next section: <a href="#" id="vagrant_lab" class="section_link">Preparing Your Lab</a>

</section>