# Ansible-PrivateRepo

What is Ansible?

Ansible is an open-source automation tool used for configuration management, application deployment, and task automation.

Why Ansible?

Ansible is needed to address various challenges in managing and automating IT infrastructure.

Key Features:

Agentless: Ansible doesn’t require any software to be installed on the nodes (managed machines). It uses SSH or WinRM to connect to these nodes and push configurations.

Declarative Language: Ansible uses YAML to write playbooks, making it easy to understand and write, even for those who are not programmers.

Idempotency: Ansible ensures that operations are performed only when necessary. For instance, if a package is already installed, Ansible will not try to install it again.

Modular Architecture: Ansible comes with a vast collection of modules that can handle tasks like installing software, managing services, and configuring files.

Common Uses:

Configuration Management: Automate the setup of servers, ensuring they have the right software, configurations, and settings.

Application Deployment: Deploy applications consistently across multiple servers.

Orchestration: Manage the execution of tasks across multiple servers in a specific order.

Provisioning: Set up the necessary infrastructure, such as virtual machines, containers, or cloud services.


Install ansible on master node?
Installing Ansible on a master node (often referred to as the "control node") is straightforward. The master node is where Ansible is installed and from which commands are executed to manage other nodes (also called "managed nodes" or "hosts"). Here's how you can install Ansible on a master node:
Prerequisites
Operating System: The control node should be running a Unix-like operating system (e.g., Linux or macOS). 
Python: Ansible requires Python 3.8 or higher to be installed on the control node.

Ansible Installation:

1. Update the System : First, update the package lists on your system:

sudo apt update  # For Debian/Ubuntu
sudo yum update  # For CentOS/RHEL

2. Install Ansible Using the Package Manager 

On Ubuntu/Debian
sudo apt install -y ansible

On CentOS/RHEL: Enable the EPEL repository if it's not already enabled:

sudo yum install -y epel-release

Install Ansible:

sudo yum install -y ansible

On Fedora

sudo dnf install -y ansible

3. Verify the Installation

Once Ansible is installed, verify the installation by checking the version:

ansible --version

4. Install Ansible via pip (Python Package Manager)
If you prefer or need a specific version of Ansible, you can install it via pip.

Install pip (if not already installed)

sudo apt install -y python3-pip  # Ubuntu/Debian
sudo yum install -y python3-pip  # CentOS/RHEL

Install Ansible via pip

pip3 install ansible

Install Specific Version of Ansible using pip

sudo pip install ansible==2.4

You won't be able to see the below inventory and config files when you install ansible via pip. Hence, you have to create below files manually.

Inventory file -> /etc/ansible/hosts
Config file -> /etc/ansible/config.cfg

What is a playbook?

An Ansible playbook is a YAML file that defines a series of tasks to be executed on remote hosts. Unlike ad-hoc commands, which are used for one-off tasks, playbooks are used to automate complex workflows and configuration management across multiple systems in a repeatable and structured way.

What are Ansible Roles?

Ansible Roles are a way to organize Ansible playbooks into reusable and modular components. Roles allow you to break down complex playbooks into smaller, more manageable parts by grouping related tasks, variables, files, templates, and handlers into a structured format. This makes it easier to manage and reuse code across different projects.


Directory Structure of an Ansible Role

A typical role might look like this:

my_role/
├── defaults/
│   └── main.yml
├── files/
│   └── myfile.conf
├── handlers/
│   └── main.yml
├── meta/
│   └── main.yml
├── tasks/
│   └── main.yml
├── templates/
│   └── mytemplate.j2
├── tests/
│   ├── inventory
│   └── test.yml
├── vars/
    └── main.yml


