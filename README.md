# ansible

## Why ansible famous

---
1)Ansible is an agent-less software
2)Ansible uses SSH as a default mechanism to communicate to other servers(PORT 22)
3)The only thing that ansible node need is a communiation to other servers that need CM
4)Ansible is a configuration tool which works both with push and pull mechanism
5)common credentials across the board(ex ssh to any of the server)
6)Ansible goes by declerative approach and their documentation is areally vast and good
7)Multiple opertions are parellel with ansible
8)Code doent need to be on the top of a local server
---
## Important points to be noted:
1) Ansible in backend uses python!!
3) When you install ansible, by default it install "ansible version2 which is from python2"
3) Python2 is expired on Jan2020
4) Latest version of ansible are phython3 based( so install ansible>2, python 3 is required)
5) By default all AWS AMI's you will get python2

## Ansible documantation reference
https://docs.ansible.com/ansible/latest/index.html


Ansible is a Open Source -->RedHat-->IBM

## INVENTORY File

Inventory is nothing but the list of machines ip or dns names that you want ansible to manage.



# How to run ansible commands, there are 2 ways
    1)manual approach   ( You can execute one action at a time)
    2)automated approach ( You can execute multiple actions parallely using playbook)

# Manual approach
    Examole :- $ ansible -i inv all -e ansible_user=centos ansible_password=DevOps321 -m shell -a uptime

# How to check all the machine up or not using ansible(very famous interview question)
    Example : $ ansible -i inv all -m ping -e ansible_user=centos -e ansible_password=DevOps321

# What is playbook?
    Playbook is an ansible script to execute things parallely
    Palybook is a list of play, Play is a list of task, task is an action you want to execute

# what is the language used by playbook
    YAML is the language  used by Ansible to write playbook
    YAML is indentation specific

# YAML is a yet another markup languate
    Markup language is a presentation language Example HTML, XML

# YAML is about 3 ways of representing data that is based on the datatype
    1) Dictonary : a key value pair
    example: course: devops
    2)List      : a key with multiple value
    Example: Course:
                    -DEVOPS
                    -AWS
                    -GCP

# How to run ansible-playbooks?
 $ ansible-playbook i inv all -m ping -e ansible_user=centos -e ansible_password=DevOps321 playbookname.yaml

# For variable when to use quotes in ansible playbooks?
 Ansible support quotes for variables, 
 
 when you are just using the varialble only then you dont need to place quotes insted use it directly {{ENV}}

 when you are  the varialble between line only then place quotes insted  example " Name of the environment {{ENV}}"



