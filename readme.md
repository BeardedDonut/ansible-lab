# Ansible Lab Repo
This is a repo where you can create an ansible lab setup and start learning ansible.
This setup helps to create a docker environment where you can setup ansible and start learning ansible.
Using docker as an option for learning ansible is better since it is light-weight solution compared to having VMs and can be easily created. Also, in case if you make a mistake you can easily create your environment using the `docker-compose` file.


# Ansible Setup:
There are three types of **working** hosts and one **controller** host in this project. Feel free to change them as you wish. the roles in this setup is as follows:

1. **Loadbalancer**: A tier of hosts running Nginx as loadbalancer
2. **Web-Server**: A tier of hosts running Apache as the web server
3. **Database**: Database tier running MysqlDB
4. **Controller**: Controller node that runs Ansible and automates the configuration of above-mentioned nodes

**NOTE**: checkout the docker-compose file to change the number of each machine. The current version of the docker-compose file creates the environment below: 

![System Architecture](./system-diagram.png)


# Ansible playboos:
the `ansible` directory contains all the required playbooks and templates to appropriately setup this environment.

