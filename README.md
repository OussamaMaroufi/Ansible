# Ansible Project


# Project Ansible integration with Jenkins 

- we installed tools(Kubectl , terraform) inside the jenkins server / container to make them available to use in the pipeline 
==> So , the commands were available for jenkins jobs 

** Instead of installing Ansible in jenkins server we Create a dedicated server for Ansible .


we can run ansible locally or remotly from dedicated server .

ansible and jenkins are runing in different server 

_ execute Ansible Playbook from jenkins pipeline to configure 2 droplet (install docker and docker compose in them)


* Connect Pipeline  to java maven Project 
* Creta a jenkins Pipeline that execute Ansible Playbook on the remote Ansible Server . and that playbook will configure tow droplet by installing docker and docker-compose .
 


 - we need t install 2 python modules : boto3 and botocore to use them in ansible to configure instances .

we need aws credntials 

also we gonna use dynamic inventory : instead of hard code ip addr of ec2 instance => get them dynamically from aws . and we need aws credentils for dynamic inventory to work fine .


# aws_ec2 inventory try to connect to aws account and fetch ec2 instances 

so we need to authenticate to aws : using credentials 

cred are stored in .aws/credentials


Launch 2 AMI in AWS (download the key-pair bcz ansible uses ssh to connect to those instnaces )


### PART 2 

** Copy file from jenkins to Ansible server .

necessary files that we need to copy them to ansible server are  : 

- the playbook itself contain the steps that will executed in managed node .

- hosts file or inventory file in our case we gonna use dynamic inventory file 

- and ansible.cfg  /* contain the configuration of ansible */


--> we need to copy all of this file to our repo directory so jenkins can access them and copy them to ansible control node .


jenkins Pipeline trigger a a call to ansible playbook 









