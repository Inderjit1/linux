# Assignment Overview: Discovering VMX Features

**CMPE 283 Virtualization - Assignment 1**

**Team Members: Inderjit Bassi, Eugene Clewlow**

## Question 1 - For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched.
Inderjit Bassi - I implemented mapping (locating and incorporating from the SDM) the primary process based, secondary processed base, entry and exit control structures from the SDM to the C file. In addition to implementing the primary process based, secondary processed base, entry and exit controls in the detect_vmx_features function (performs the rdmsr, pr_info and report_capability).

Eugene Clewlow - I implemented the check for activating secondary controls in primary processes base controls before performing msr reads of secondary processes based controls.  I also built the Linux kernel and built and installed the module.

## Questin 2 - Describe in detail the steps you used to complete the assignment. Consider your reader to be someone skilled in software development but otherwise unfamiliar with the assignment. Good answers to this question will be recipes that someone can follow to reproduce your development steps.

To complete this assignment, a distro of Linux (any version) was required. The one used for this was Ubuntu 20.04 LTS. After installing this .iso image on VirtualBox and VMWare, there are few packages that need to be installed. Needed to install the following: git, make and all of the necessary gcc compilation packages. 

1) The commands to run inside the VM are listed as the following (downloads and installs git, make and gcc packages):
```
    $ sudo apt-get install git fakeroot build-essential ncurses-dev xz-utils libssl-dev bc flex libelf-dev bison
```

2) The Linux kernel (from torvalds/linux) was forked to this repository. Next, the fork was cloned on the VM using the command:
``` 
    git clone https://github.com/Inderjit1/linux.git
```

** 3. Steps 3-6 are not required for assignment 1 but doing these steps sets us up to work on assignment 2.**

4) Configuration was copied using:
```
  $ sudo cp /boot/config-5.8.0-48-generic ./.config
```

5) The kernel was configured using:
```
  $ sudo make oldconfig
```

** 6. The kernel was built with (note: -j 8 refers to the number of CPUs you have assigned to the VM instance, this number varies based on how each VM is setup): **
```
    $ make -j 8 modules && make -j 8
```

7) A branch was created to store the msr reading module code here: https://github.com/Inderjit1/linux/tree/VMX_ASSIGNMENT. The repository contains two relevant files: cmpe283-1.c and Makefile.

8) The kernel module can be built using:
```
  $ git checkout VMX_ASSIGNMENT
  $ make
```

9) Installed using:
```
  $ sudo insmod cmpe283-1.ko
```

10) and uninstalled using:
```
  $ sudo rmmod cmpe283-1
```

11) To view output of the kernel:
```
  $ sudo dmesg
```

The kernel message output of the module that we received when installing the module ourselves can be viewed here. 
https://github.com/Inderjit1/linux/blob/VMX_ASSIGNMENT/output.txt
