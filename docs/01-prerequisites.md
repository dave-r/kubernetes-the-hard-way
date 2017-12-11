# Prerequisites

## QEMU/KVM and virt-manager

This tutorial leverages QEMU/KVM and the virt-manager UI to provision the compute infrastructure required to bootstrap a Kubernetes cluster from the ground up. 

### Install QEMU/KVM and virt-manager

Ensure that QEMU/KVM and virt-manager are installed.

* https://www.qemu.org/
* https://www.linux-kvm.org
* https://virt-manager.org/
* https://libvirt.org/
* https://fedoraproject.org/wiki/Getting_started_with_virtualization
* https://wiki.archlinux.org/index.php/QEMU

Verify the tools are installed:

```
$ qemu-system-i386 -version  	# verify qemu
$ modinfo kvm 					# verify kvm
$ virt-manager --version		# verify virt-manager UI tool
```

### Create a virtual network

This tutorial assumes a virtual network is configured as follows
* Name : kube-net
* IPv4 network address space : 10.240.0.0/24
* DHCPv4 disabled
* IPv6 address space disabled
* Connect to a physical network
	* Forwarding to Physical network
	* Destination : Any physical device
	* Mode : NAT

Next: [Installing the Client Tools](02-client-tools.md)
