# kernel-dev

A Vagrantfile and setup instructions for my personal kernel development setup.

## Setup

```
git clone git@github.com:apache8080/kernel-dev.git
cd kernel-dev
mkdir modules
vagrant up
```

The `modules` directory is where you can put all your new kernel modules and this folder is a Vagrant synced folder.

## Workflow
Write code on host machine and run the following:
```
vagrant rsync-auto
```

This will have a watcher on the synced folder and rsync it to the VM when ever changes are made.

In a separate terminal you can `vagrant ssh` into the VM and build and test your modules.