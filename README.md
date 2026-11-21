# Project 15: Automate Server Configuration with Ansible

## Objective
Automate Nginx web server installation and configuration using an Ansible playbook.

## Technologies Used
- Ansible
- Ubuntu Linux
- Nginx
- YAML
- Git and GitHub

## Implementation
1. Installed Ansible on the Linux VM.
2. Configured localhost as the Ansible managed host.
3. Verified connectivity using the Ansible ping module.
4. Created a playbook to install Nginx.
5. Deployed a custom HTML webpage using Ansible.
6. Started and enabled the Nginx service.
7. Verified the webpage using curl.
8. Verified playbook idempotency.

## Commands

Test connectivity:
    ansible -i inventory.ini webservers -m ping

Execute playbook:
    ansible-playbook -i inventory.ini playbook.yml

Verify webpage:
    curl http://localhost

Verify Nginx:
    sudo systemctl status nginx

## Results
- Nginx installed successfully.
- Webpage deployed successfully.
- Nginx service active and running.
- Ansible playbook completed without failures.

## Note
This implementation uses localhost because outbound SSH access
from the company VM to AWS EC2 was unavailable.
Remote configuration was not demonstrated.

## Conclusion
Successfully demonstrated automated Nginx installation and configuration
using Ansible on localhost.
