# Puppet Installation on Linux

These instructions will guide you through the process of installing puppet master and agent

## Step 1  - Install Puppet Master and Agent

In this step, you are required to install Puppet Master and Agent Servers. Master should be a single server, agents can be in any number depending upong how many servers you want to setup for your Lab  

All the commands should be performed as `root` user. Become `root` user by issuing below command and provide password   

`sudo su -`

Now you are required to create a directory and go inside directory  

`mkdir puppet`  
`cd puppet`

Install `wget` package    

`yum install wget -y`

Now download the below mentioned rpm file from `https://yum.puppetlabs.com/` based on your operationg system. In below example, we are taking CentOS-6    

`wget https://yum.puppetlabs.com/puppetlabs-release-el-6.noarch.rpm`   

Install the rpm downloaded in above step

`rpm -ivh puppetlabs-release-el-6.noarch.rpm`   


Now install `puppetserver` on Master node    

`yum clean all`   
`yum update -y`   
`yum install puppetserver`   


### Install Puppet Master and Agent
### Edit the host and Puppet Configuration files in both Puppet Master & Agent
### Establish secure connection between Master and Agent
