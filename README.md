# Capture The Flag Challenges for eBPF Summit 2022

Challenge 1 is a quiz. This repo hold the instructions for setting up for challenges 2 and 3. 

These challenges require a recent Linux kernel with BTF support. We've tested it
on Ubuntu 22.04 in a virtual machine and we're providing config for Lima-VM and
a Vagrantfile. Note: this challenge is unlikely to work on LinuxKit so running
in Docker, or with kind on Mac/Windows, is not recommended.  
## Deploying the challenges

* On Mac, you can set up the challenges using Lima-VM by running `limactl start
  cilium.yaml` with the file provided in this repo. Once this completes, open a shell into the VM with `limactl
  shell cilium`.

* If you're a Vagrant user, we've supplied a Vagrantfile for you as well. Download that file and run
  `vagrant up`. Once this is finished, run `vagrant ssh` to open a shell into
  the VM.

If you don't want to use Lima or Vagrant, set up a Kubernetes or K3s cluster
that uses Cilium as its CNI, and apply the config YAML from [here](https://gist.githubusercontent.com/lizrice/107e492b82f386da8883e9d1a385c0b2/raw/ctfapp.yaml). 

# The challenges

## Challenge 1 

Challenge 1 was a quiz that we played during day 1 of eBPF Summit 

## Challenge 2

You won't need Kubernetes knowledge for this challenge. Like a treasure hunt, a **map** will show you the way.

Set up the VM as described above. Once it's up and running, open a shell / SSH into it.

Follow the instructions at https://isogo.to/summit-2022-ctf-2. 

> **Note**
>
> If you want to see the solution, watch the live solving session from [eBPF Summit 2022 Day 2](https://youtu.be/a3AwA1VdohU?t=9240)

## Challenge 3

You can use the same VM for this challenge. Open a shell / SSH into it and run `kubectl get pods`. You
should find one pod running in the default namespace. It might take a couple of
minutes to get to ready state if you've only just deployed it.
 
Once it's up and running, the application executing in that pod will tell you what you need to do.

Check your answer or get hints at https://isogo.to/summit-2022-ctf-3 

> **Note**
>
> If you want to see the solution, check out [episode 64](https://youtu.be/CBUIy0FzxFY) of [eCHO livestream](https://github.com/isovalent/eCHO)
