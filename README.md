# Ansible-automation

#  What is Ansible?

Ansible is simply an open-source IT engine that automates application deployment, intra service orchestration, cloud provisioning, and many other IT tools.
Ansible is easy to deploy because it does not use any agents or custom security infrastructure.
Ansible uses playbook to describe automation jobs, and playbook uses very simple language i.e. YAML (It’s a human-readable data serialization language & is commonly used for configuration files, but could be used in many applications where data is being stored) which is very easy for humans to understand, read and write. Hence the advantage is that even the IT infrastructure support guys can read and understand the playbook and debug if needed (YAML – It is in human-readable form).
Ansible is designed for multi-tier deployment. Ansible does not manage one system at a time, it models IT infrastructure by describing all of your systems are interrelated. Ansible is completely agentless which means Ansible works by connecting your nodes through ssh(by default). But if you want another method for connection like Kerberos, Ansible gives that option to you.
After connecting to your nodes, Ansible pushes small programs called “Ansible Modules”. Ansible runs those modules on your nodes and removes them when finished. Ansible manages your inventory in simple text files (These are the hosts file). Ansible uses the hosts file where one can group the hosts and can control the actions on a specific group in the playbooks.

# Advantages of Ansible
- Free: Ansible is an open-source tool.
- Very simple to set up and use: No special coding skills are necessary to use Ansible’s playbooks (more on playbooks later).
- Powerful: Ansible lets you model even highly complex IT workflows.
- Flexible: You can orchestrate the entire application environment no matter where it’s deployed. You can also customize it based on your needs.
- Agentless: You don’t need to install any other software or firewall ports on the client systems you want to automate. You also don’t have to set up a separate management structure.
- Efficient: Because you don’t need to install any extra software, there’s more room for application resources on your server.

# What is Configuration Management?
Configuration management in terms of Ansible means that it maintains the configuration of the product performance by keeping a record and updating detailed information that describes an enterprise’s hardware and software.
Such information typically includes the exact versions and updates that have been applied to installed software packages and the locations and network addresses of hardware devices. E.g., If you want to install the new version of the WebLogic/WebSphere server on all of the machines present in your enterprise, it is not feasible for you to manually go and update every machine.
You can install WebLogic/WebSphere in one go on all of your machines with Ansible playbooks and inventory are written most simply. All you have to do is list out the IP addresses of your nodes in the inventory and write a playbook to install WebLogic/WebSphere. Run the playbook from your control machine & it will be installed on all your nodes.

# How Ansible Works?
The picture given below shows the working of Ansible.
Ansible works by connecting to your nodes and pushing out small programs, called "Ansible Modules" to them. Ansible then executes these modules (over SSH by default) and removes them when finished. Your library of modules can reside on any machine, and there are no servers, daemons, or databases required.

![image](https://user-images.githubusercontent.com/66211088/158861240-3607eeb3-60a0-4fd1-be1e-0a098ec68a39.png)

The management node in the above picture is the controlling node (managing node) which controls the entire execution of the playbook. It’s the node from which you are running the installation. The inventory file provides the list of hosts where the Ansible modules need to be run and the management node does an SSH connection and executes the small modules on the host's machine and installs the product/software.
