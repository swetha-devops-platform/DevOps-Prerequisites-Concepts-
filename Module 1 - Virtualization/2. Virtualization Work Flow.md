Work Flow of Virtualization: 

Terminologies : 

      Host OS - Operating system on Physical Computers
      
      Guest OS - Operating system of Virtual Machine. 
      
      VM - Virtual Machine [ it is nothing but Sorts of file ] 
      
      Snapshot 
      
      Hypervisor 

How it Works : 
      
      There will be one physical server
      
      Hypervisor is installed.
      
      A Hypervisor will create an VM.
      
      Each VMs runs on its own Operating system, Application and have its own configuration. 

Each VM will be act as an " Separate Real Computers " 

Work Flow Architecture : 

<img width="256" height="243" alt="Image" src="https://github.com/user-attachments/assets/47098763-74f3-4130-8cdc-79d6b322504b" />

Hypervisor : 

      Hypervisor is a tool or software which is used to create an Virtual machine.

      It Allocates resources to the virtual machine. 

      It Manages VM Lifecycle. 

Types of Hypervisor : 

Type 1 : Bare Metal Hypervisor { Runs Directly on Software } 

       It is only for Production purpose and it is faster and more secure. 

       Example : VMwareEsxi, Microsoft hyperV, Xen. 

Type 2 : Hosted Hypervisor { Runs on top of OS } 

        It is only for learning and testing purpose, Esay to use and it is slower.

        Example : Oracle VirtualBox.

Snapshot : 

          A snapshot is a point-in-time copy of a Virtual Machine that captures its disk state, configuration, and sometimes memory, so you can roll back the VM to that exact moment if something goes wrong.

          Snapshot is NOT a backup.

          In Simple Words - " A snapshot allows you to restore a VM to a previous state." 
    
