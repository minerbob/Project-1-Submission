## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

Project-1-Submission\Diagrams\homework12.html.pdf)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  Project-1-Submission\Ansible\ELK.yml

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly avialable, in addition to restricting access to the network.
- _TODO: What aspect of security do load balancers protect? efends an organization against distributed denial-of-service (DDoS) attacks
 What is the advantage of a jump box?
secure computer that all admins first connect to before launching any administrative task or use as an origination point to connect to other servers or untrusted environments
or in otherwords secure centerlised managment

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the network and system files.
- _TODO: What does Filebeat watch for?_ filebeat monitors the log files or locations that you specify, collects log events,
- _TODO: What does Metricbeat record?_ Metricbeat helps you monitor your servers by collecting metrics from the system and services

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| Web-1    | Webserver| 10.0.0.5   | Linux            |
| Web-2    | Webserver| 10.0.0.6   | Linux            |
| ElkSVR   | ELKserver| 10.1.0.4   | Linux            |


### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 73.242.65.23

Machines within the network can only be accessed by ElkSVR.
- 10.1.0.4

A summary of the access policies in place can be found in the table below.

| Name     | Publicly Accessible | Allowed IP Addresses |
|----------|---------------------|----------------------|
| Jump Box | Yes                 | 10.0.0.1 10.0.0.2    |
|ELK server| Yes                 | 10.0.0.1 10.0.0.2
|          |                     |                      |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- ease of rebuilding or disaster recovery, consitncy of builds. 

The playbook implements the following tasks:
- name: docker.io
    apt:
      force_apt_get: yes
      update_cache: yes
      name: docker.io
      state: present
Install Doceker

  - name: Install pip3
    apt:
      force_apt_get: yes
      name: python3-pip
      state: present
Install Python

  - name: Install Docker python module
    pip:
      name: docker
      state: present
Install python module
T
### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- 10.0.0.5 and 10.0.0.6

We have installed the following Beats on these machines:
- 10.0.0.5 and 10.0.0.6

These Beats allow us to collect the following information from each machine:
beat that collects and reports various system-level metrics for various systems and platform

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:

_TODO: Answer the following questions to fill in the blanks:_
- Copy the Elk.yml file to Elk_install.yml.
- Update the host file to include 10.1.0.4 anible_python_interpreter=/usr/bin/python3
- Run the playbook, and navigate to http://73.242.65.23:5601/app/kibana to check that the installation worked as expected.
