[comment]: <> (please keep all comment items at the top of the markdown file)
[comment]: <> (please do not change the ***, as well as <div> placeholders for Note and Tip layout)
[comment]: <> (please keep the ### 1. and 2. titles as is for consistency across all demoguides)
[comment]: <> (section 1 provides a bullet list of resources + clarifying screenshots of the key resources details)
[comment]: <> (section 2 provides summarized step-by-step instructions on what to demo)


[comment]: <> (this is the section for the Note: item; please do not make any changes here)
***
### Service-endpoints-and-securing-storage

<div style="background: lightgreen; 
            font-size: 14px; 
            color: black;
            padding: 5px; 
            border: 1px solid lightgray; 
            margin: 5px;">

**Note:** Below demo steps should be used **as a guideline** for doing your own demos. Please consider contributing to add additional demo steps.
</div>

[comment]: <> (this is the section for the Tip: item; consider adding a Tip, or remove the section between <div> and </div> if there is no tip)

***
### 1. What Resources are getting deployed

#### Scenario
You have been asked to create a proof of concept to demonstrate securing Azure file shares. Specifically, you want to:

Create a storage endpoint so traffic destined to Azure Storage always stays within the Azure backbone network.
Configure the storage endpoint so only resources from a specific subnet can access the storage.
Confirm that resources outside of the specific subnet cannot access the storage.

Resources deployed: 

 - myVMPrivate_OsDisk_1 and 2: VM disks
 - myVmPublic_OsDisk_1 and 2: VM disks
 - MyVM1NiC and MyVM2Nic: network interfaces
 - myNsgPrivate and MyNsgPublic: Network security groups
 - MyVmPrivate-ip: Private IP address
 - MyVmPublic-ip: Public IP Address
 - storage-rgname: storage account
 - MyVmPublic and MyVmPrivate: Virtual machines
 - myVirtualNetwork: virtual  network

<img src="https://raw.githubusercontent.com/daverendon/azd-service-endpoints-and-securing-storage/refs/heads/main/demoguide/rg-service-endpoints-and-securing-storage.png" alt="Intersite connectivity" style="width:70%;">
<br></br>
<br></br>

### 2. What can I demo from this scenario after deployment

This demo guides you through a hands-on exercise to build and secure a networked environment in Azure. You will start by creating a virtual network and adding a subnet with a configured storage endpoint. Next, you will implement network security groups—first to restrict access to the private subnet and then to allow RDP access on the public subnet. Following this, you will create a storage account with a file share and deploy virtual machines into their respective subnets. Finally, you will test the storage connection from both the private and public subnets to verify that access is correctly allowed from the private subnet and denied from the public subnet.

<img src="https://raw.githubusercontent.com/daverendon/azd-service-endpoints-and-securing-storage/refs/heads/main/demoguide/diagram-service-endpoints-and-securing-storagey.png" alt="Intersite connectivity diagram" style="width:70%;">
<br></br>
<br></br>

[comment]: <> (this is the closing section of the demo steps. Please do not change anything here to keep the layout consistant with the other demoguides.)
<br></br>
***
<div style="background: lightgray; 
            font-size: 14px; 
            color: black;
            padding: 5px; 
            border: 1px solid lightgray; 
            margin: 5px;">

**Note:** This is the end of the current demo guide instructions.
</div>


