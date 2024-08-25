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
