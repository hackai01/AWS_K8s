# AWS_K8s
Local Ansible infrastructure setup for AWS config (This guide assumes the host controller is UbunutuOS)

Ensure you ENV is upto date - sudo apt -y update && sudo apt -y upgrade
Create AWS Account. (If you already have an acc skip this)
Create IAM User with Admin Creds. Take note of the Secret Key and ID
Install the following packages
- Python3 sudo apt -y install python3
- pip3 - sudo apt -y install python-pip3
- boto, boto 3 and Ansible - pip3 install boto boto3 ansible
Check Installation
ansible -- version

You should see the following

ansible [core 2.13.1]
  config file = None
  configured module search path = ['/home/hacaki/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /home/hacaki/.local/lib/python3.10/site-packages/ansible
  ansible collection location = /home/hacaki/.ansible/collections:/usr/share/ansible/collections
  executable location = /usr/bin/ansible
  python version = 3.10.4 (main, Apr  2 2022, 09:04:19) [GCC 11.2.0]
  jinja version = 3.1.2
  libyaml = True
  
Run "aws configure"
- Input IAM secret key and ID you noted down earlier

There is a host file in this repo that I am not using but will be doing at some point. You many need to specify the python onterpriter but Ive done that in my local host file for the local input. Let me know if youre having issues.

Grab a playbook from the repo like the create ec2 yaml and see if it works.
