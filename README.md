**TODO**
* Make this repo public when we are ready to go live

# Capture The Flag Challenge for eBPF Summit 2022

This challenge requires a recent Linux kernel with BTF support. We've tested it on Ubuntu 22.04 in a virtual machine. 

## Deploying the challenge 

Start by cloning this repo. 

We have provided config for running in Lima-VM or Vagrant. 

* On Mac, you can set up this challenge using Lima-VM by running `limactl start cilium.yaml`. Once this completes, open a shell into the VM with `limactl shell cilium`,

* If you're a Vagrant user, we've supplied a Vagrantfile for you as well. Run `vagrant up`. Once this is finished, run `vagrant ssh` to open a shell into the VM. 

If you don't want to use Lima or Vagrant, set up a Kubernetes or K3s cluster that uses Cilium as its CNI, and run `kubectl apply -f ctfapp.yaml`. 

Note: this challenge is unlikely to work on LinuxKit so running in Docker, or with kind on Mac/Windows, is not recommended. 

# The challenge

Once the VM is up and running, SSH into it and run `kubectl get pods`. You should find one pod running (in the default namespace). It might take a couple of minutes to get to ready state. Once it's up and running, the application executing in that pod will tell you what you need to do.

Submit your answers at https://isogo.to/summit-2022-ctf
