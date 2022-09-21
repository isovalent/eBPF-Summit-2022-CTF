# Capture The Flag Challenge for eBPF Summit 2022

This challenge requires a recent Linux kernel with BTF support. We've tested it on Ubuntu 22.04 in a virtual machine. 

## Deploying the challenge 

Start by cloning this repo. 

We have provided config for running in Lima-VM or Vagrant. 

* On Mac, you can set up this challenge using Lima-VM by running `limactl start cilium.yaml`

* If you're a Vagrant user, we've supplied a Vagrantfile for you as well. Run `vagrant up`. 

If you don't want to use Lima or Vagrant, set up a Kubernetes or K3s cluster that uses Cilium as its CNI, and run `kubectl apply -f ctfapp.yaml`. 

Note: this challenge is unlikely to work on LinuxKit so running in Docker, or with kind on Mac/Windows, is not recommended. 

# The challenge

Once the VM is up and running you should find it's running a Kubernetes pod.
The application running in that pod will tell you what you need to do.
