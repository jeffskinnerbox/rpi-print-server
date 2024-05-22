<!--
Maintainer:   jeffskinnerbox@yahoo.com / www.jeffskinnerbox.me
Version:      0.0.0
-->


<div align="center">
<img src="https://raw.githubusercontent.com/jeffskinnerbox/blog/main/content/images/banners-bkgrds/work-in-progress.jpg" title="These materials require additional work and are not ready for general use." align="center" width=420px height=219px>
</div>


-----


# The Zen of Ansible
"The Ansible way" is to provide an automation tool that is simple, powerful and agentless. Ansible enables users with no special coding skills to do powerful things across multiple IT domains. Its human readable automation can be utilized and shared by every IT team so they can get productive quickly and contribute their expertise. Its agentless architecture provides the flexibility to be applied across all IT infrastructure domains.

* [The Zen of Ansible](https://www.ansible.com/blog/the-zen-of-ansible/)
* [Ansible Code Testing — Part 1 — Test Environment Automation](https://medium.com/@m.h.azaddel/ansible-code-testing-part-1-test-environment-automation-36f3983d9c2f)
* [Ansible Code Testing — Part 2 — Writing Tests](https://medium.com/@m.h.azaddel/ansible-code-testing-part-2-writing-tests-9bed51134e08)

# YAML linter
YAML linter to spot Ansible YAML syntax errors

```bash
# yaml linter to spot Ansible YAML syntax errors
yamllint rpi-docker.yml
ansible-lint rpi-docker.yml
```

# Static Analysis
We need a linter or a tool to just check syntax issues

## Ansible Syntax Checker
Ansible linter to spot Ansible playbook syntax errors

```bash
# ansible linter to spot Ansible playbook syntax errors
ansible-playbook rpi-docker.yml -i 192.168.1.207, --user ansible --syntax-check
```

## List Ansible Tasks to be Executed
Generate a list of tasks that will be executed for the tags

```bash
# generate a list of tasks that will be executed for the tags
ansible-playbook rpi-docker.yml -i 192.168.1.207, --user ansible --list-tasks
```

## Ansible Dry-Run Checking
Ansible dry-run checking for errors and showing results of a run

```bash
# ansible dry-run checking for errors and showing results of a run
ansible-playbook rpi-docker.yml -i 192.168.1.207, --user ansible --check
```

## Check Ansible Playbook's Idempotence
Check for Ansible Playbook's idempotence

```bash
# check for Ansible Playbook's idempotence
ansible-playbook rpi-docker.yml -i 192.168.1.207, --user ansible --check --diff --limit
```

# Unit Test
Same as a Unit test in a programming language. Take each Ansible Task as a unit. To provide a test environment we use [Molecule](https://github.com/ansible-community/molecule) and to test the results after applying our ansible codes we can some test libraries like Testinfra, Goss, etc.

* [Rapidly Build & Test Ansible Roles with Molecule + Docker](https://www.toptechskills.com/ansible-tutorials-courses/rapidly-build-test-ansible-roles-molecule-docker/)
* [How To Test Ansible Roles with Molecule on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-test-ansible-roles-with-molecule-on-ubuntu-18-04)
* [Testing Ansible roles with Molecule](https://opensource.com/article/18/12/testing-ansible-roles-molecule)

# Integration Test
You can take a playbook, role, or a collection as a group to be tested entirely. The same libraries are used for this level.

* [Using Testinfra with Ansible to verify server state](https://opensource.com/article/19/5/using-testinfra-ansible-verify-server-state)

# Test Ansible Collections
With Ansible,
Collections are a distribution format that can include playbooks, roles, modules, and plugins.
You can install and use collections through a distribution server, such as Ansible Galaxy, or a Pulp 3 Galaxy server.

Both ansible-core and ansible-base come packaged with a cli tool called `ansible-test`,
which can be used test Collection and its content.

* [Introduction to ansible-test](https://www.ansible.com/blog/introduction-to-ansible-test/)
* [Ansible Collections](https://www.youtube.com/playlist?list=PLdu06OJoEf2Z85Lrc7_Sdw6mTt4aSKfwt)
* [Creating a New Ansible Collection: A Step-by-Step Guide](https://www.youtube.com/watch?v=h_zp7xpIGW4)

# Ansible Builder
Ansible Builder is a tool that aids in the creation of Ansible Execution Environments.
It does this by using the dependency information defined in various Ansible Content Collections, as well as by the user. Ansible Builder will produce a directory that acts as the build context for the container image build, which will contain the Containerfile, along with any other files that need to be added to the image.

* [Introduction to Ansible Builder](https://www.ansible.com/blog/introduction-to-ansible-builder/)

