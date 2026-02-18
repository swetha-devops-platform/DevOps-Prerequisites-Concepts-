Vagrant : 

        Vagrant is a tool for creating and managing virtual development environments using configuration files, so developers can quickly create identical VMs on any system.
    
        Vagrant is also said to be an VM Automation Tool and manages the VM Lifecycle.
    
        Its not an replacement of hypervisor like oracle virtual box, vm ware but it uses these tool to create and manage the virtual machines.

        mainly for development/testing, not for production

Who Created Vagrant?

       It was created by HashiCorp, the same company that created:

            Terraform, Vault, Consul


Why Vagrant is Used: 

Without Vagrant

         Manual VM setup

         “It works on my machine” problem

          Different environments for each developer

          Time-consuming setup

With Vagrant

          One config file → same VM everywhere

          Fast setup

          Reproducible environments

          Easy teardown

Vagrant Workflow : 

Step 1 : Create an Project Directory 

<img width="387" height="58" alt="image" src="https://github.com/user-attachments/assets/7c474ba8-88a3-4e0b-8a3b-eaf6f45671a7" />

Step 2 : Create an Vagrant file from vagrant cloud boxes and placed in project directory

<img width="761" height="144" alt="image" src="https://github.com/user-attachments/assets/0bc0c61a-6975-4ed4-a418-58de624f59a1" />

Step 3 : Starting up the VM 

<img width="649" height="90" alt="image" src="https://github.com/user-attachments/assets/34b4fa6c-f414-4cbd-9a2d-915080327976" />

Step 4 : Logging into VM 

<img width="610" height="75" alt="image" src="https://github.com/user-attachments/assets/1cddf270-3cf4-4e7c-ad28-07877e3eab21" />



Common Vagrant Commands: 

             vagrant init - Create Vagrantfile
             
             vagrant up - Start VM
             
             vagrant ssh - Login to VM
             
             vagrant halt - Stop VM
             
             vagrant destroy - Delete VM
             
             vagrant status - Check state


Role of Vagrant in DevOps

         Vagrant is used for:

                  Local DevOps labs

                  Testing Ansible / Terraform

                  CI/CD experimentation

                  Infrastructure learning

Key Concepts in Vagrant - Based on Interview Based

Vagrant File : 

            A Vagrantfile is a configuration file used by Vagrant to define how a virtual machine should be created and configured.

            Vagrantfile is an Infrastructure-as-Code file that describes a VM environment.

Vagrant Box : 

            A Box is a pre-configured OS image used by Vagrant to create virtual machines.

            Example: ubuntu/focal64, centos/7.

Provider in Vagrant : 

            A Provider is the virtualization platform that Vagrant uses to create VMs.

            Common provider: Oracle VM VirtualBox, VMware, Hyper-V.

Provisioning in Vagrant : 

            Provisioning is the process of automatically installing and configuring software inside the VM after it is created.

            Types: Shell scripts, Ansible, Puppet, Chef

            Example : config.vm.provision "shell", inline: "sudo apt install -y nginx"

Synced Folder : 

            It syncs a folder between host machine and VM.

            Example: config.vm.synced_folder ".", "/vagrant"

Vagrant Networking : 

             In Vagrant, networking is used to control how the Virtual Machine (VM) communicates:

                            With the Host machine

                            With Other VMs

                            With the External network / Internet

             Vagrant supports:

                            Forwarded Port - It forwards traffic from a host machine port → guest VM port 
                            
                                             we use it to access services running inside the VM from your local browser.

                            Private Network - Private network assigns a static IP to the VM for internal communication between host and other VMs.

                            Public Network - Public network connects the VM directly to the external network using bridged mode, allowing it to behave like a real machine on the network.


            






