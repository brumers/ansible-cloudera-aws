# Cloudera - AWS Playbook
Ansible playbook to launch Cloudera on AWS

## Roles
* ec2_instance
  * Role to start up an EC2 Instances
* common
  * Configuring EC2 instances after starting them up


## Building

    ansible-playbook -e 'host_key_checking=False' ec2.yaml --private-key={private-key}
