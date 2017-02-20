# Cloudera - AWS Playbook
Ansible playbook to launch Cloudera on AWS

## Roles
* ec2_instance
  * Role to start up an EC2 Instances
* common
  * Configuring EC2 instances after starting them up


## Building

    ansible-playbook ec2.yaml --private-key={private-key}
    
 
 If you need to rerun it, create a hosts file and add, create each IP address on a difference line
     
     [launched]
     <All IP ADDRESSES>
     
     [master]
     <Master IP ADDRESSES>
     
     [slaves]
     <Slaves IP ADDRESSES>
     <Slaves IP ADDRESSES>
     <Slaves IP ADDRESSES>
     
 Then Run
     ansible-playbook  -i hosts ec2.yaml --private-key={private-key}  --limit @{FULL PATH}/ansible-cloudera-aws/ec2.retry