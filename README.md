Linux kernel
============

There are several guides for kernel developers and users. These guides can
be rendered in a number of formats, like HTML and PDF. Please read
Documentation/admin-guide/README.rst first.

In order to build the documentation, use ``make htmldocs`` or
``make pdfdocs``.  The formatted documentation can also be read online at:

    https://www.kernel.org/doc/html/latest/

There are various text files in the Documentation/ subdirectory,
several of them using the Restructured Text markup notation.

Please read the Documentation/process/changes.rst file, as it contains the
requirements for building and running the kernel, and information about
the problems which may result by upgrading your kernel.


# Assignment 2: Modifying instruction behavior in KVM 
**CMPE 283 Virtualization - Assignment 2**

**Team Members: Inderjit Bassi, Eugene Clewlow**

## Question 1 - For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched.

Inderjit Bassi - Added code to arch/x86/kvm/vmx/vmx.c to track and handle the CPUID leaf function for 0x4FFFFFFF (reading data into eax, ebx, ecx register based on requirements).

Eugene Clewlow - I added code to include/linux/kvm_host.h and arch/x86/kvm/vmx/vmx.c to keep track of cycles spent for exiting and exit count.


## Question 2 - Describe in detail the steps you used to complete the assignment. Consider your reader to be someone skilled in software development but otherwise unfamiliar with the assignment. Good answers to this question will be recipes that someone can follow to reproduce your development steps.

To complete this assignment, a distro of Linux (any version) was required. The one used for this was Ubuntu 20.04 LTS. After installing this .iso image on VirtualBox and VMWare, there are few packages that need to be installed. Needed to install the following: git, make and all of the necessary gcc compilation packages. 

*** Note: This assignment builds upon the steps listed in assignment 1 (installing Linux Kernel, make command, etc.). ***

1) Install the following libraries (QEMU is used to install KVM, Virt-Manager is used to manage VM installations):
```
    sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt-manager
```

2) Verify KVM Installation with either command listed below (output window should show no errors):
```
    sudo virsh -c gemu://system list 
    sudo virsh list --all
```

3) Verify KVM virtualization is enabled on machine (“KVM acceleration can be used” should be displayed):
```
    kvm -ok 
```

4) Follow the necessary steps for downloading an .iso and qcow file(s):
    * Download the iso image for any Linux distribution(s), example: 
        ```
           sudo wget https://releases.ubuntu.com/20.04/ubuntu-20.04.2-live-server-amd64.iso
          ```
    * Create disk image used by QEMU
        ```
            sudo qemu-img create -f qcow2 ubuntu.qcow 20G
        ```
5) Startup Virtual Manager setup:
```
    sudo virt-manager
```

6) Follow the installation steps and the VM installation should be up and running. Here is a great documentation guide that details virtual manager setup: https://phoenixnap.com/kb/ubuntu-install-kvm

## Question 3- Comment on the frequency of exits – does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations? Approximately how many exits does a full VM boot entail? 

The frequency of exits that inside the KVM occurs at a fairly stable rate - this is dependent on the VM operations that are being performed. The stable rate means the number of exits for most common VM operations executed for a VM within a VM occur at the same measured rate. Depending on the types of exits and exit handling controls enabled, the number of exits performed vary. Based on the VM(s) installed during out tests, the number of cycles varied and the range was between: 1-3 million exits.


# Assignment 3: Instrumentation via hypercall 
**CMPE 283 Virtualization - Assignment 3**

**Team Members: Inderjit Bassi, Eugene Clewlow**

## Question 1 - For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched.

Inderjit Bassi -

Eugene Clewlow - I added code to the KVM (specifically the Intel KVM/VMX) to keep track of the exit types and exit counts.


## Question 2 - Describe in detail the steps you used to complete the assignment. Consider your reader to be someone skilled in software development but otherwise unfamiliar with the assignment. Good answers to this question will be recipes that someone can follow to reproduce your development steps.

A new count tracking code implementation needed to be added to the VMX, one that could count multiple exit types at once.  So we used an array as a data structure to handle the counting.  We also needed code in the cpuid emulation to handle the new leaf requirement.

Once our code changes were done, we rebuilt the kernel and installed it.

We wrote code to test our changes and in order to answer Questions 3 & 4


## Question 3 - Comment on the frequency of exits – does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations? Approximately how many exits does a full VM boot entail?

A full VM boot entails 1,971,700 exits.  The exits increase at a somewhat stable rate.  The EXIT_REASON_HLT exit, for example seems to increase at a stable rate.  We think it also depends somewhat on the user's activity.  Quite a few exits occured at VM boot.  It seems that editing files tends to cause the EXIT_REASON_MSR_WRITE to increase substantially.

## Question 4 - Of the exit types defined in the SDM, which are the most frequent? Least?

The most frequent exit types are:
EXIT_REASON_MSR_WRITE, EXIT_REASON_HLT, & EXIT_REASON_MSR_READ

The least frequent exit types, just to name a few (there are many exit types that have exit count of 0) are:
EXIT_REASON_TRIPLE_FAULT, EXIT_REASON_NMI_WINDOW, & EXIT_REASON_TASK_SWITCH
