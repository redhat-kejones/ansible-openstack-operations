# ansible-openstack-operations
This repo will be a collection of playbooks to handle common operations on an OpenStack cloud

## Repo Uses Python virtualenv to lockdown python dependencies

Install virtualenv onto your ansible host

```
$ virtualenv ansible-openstack-operations

$ cd ansible-openstack-operations

$ . bin/activate

$ pip install -r requirements.txt
```

At this point you will have a virtual environment that has all the necessary dependencies.

Copy the vars example file and modify to fit your needs.

```
$ cp vars/vars.example.yml vars/vars.yml
$ vi vars/vars.yml
```


Now you can run the first playbook to test connectivity to your OpenStack cloud

```
$ ansible-playbook -i inventory/inventory.yml -e@vars/vars.yml playbooks/test_api_connection.yml
```
