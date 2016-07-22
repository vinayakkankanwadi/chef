# chef
Automatically configuring node onto the VM using chef.

Required:

chef-solo (chef-dk)
https://downloads.chef.io/chef-dk

Step 1: Create vm using 
	vagrant init ubuntu/trusty64

Step 2: Bring up VM and check Node(which should not be present)
	vagrant up
    vagrant ssh
	node -v 

Step 3:	Generate cookbook. This will create Berksfile which we will be using to install packages.
	chef generate cookbook my_cookbook
	cd my_cookbook
    mkdir cookbooks

Step 4: Update Berksfile with required cookbooks then call below cmd to update cookbooks	
    berks vendor cookbooks

Step 5: Update VagrantFile with cookbook path and receipies to be installed in VM

Step 6: Provision the VM
    vagrant provision
	[if issues with vigrant up one may have to do vagrant reload then do vagrant provision]

Step 7: Check node on VM(node should be installed)
    node -v 
vagrant ssh or using putty ssh into the box and check node is installed using node -v