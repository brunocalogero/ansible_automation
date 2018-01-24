# ansible_automation
Automate your day to day ad hoc manual network engineering tasks using Ansible!

## Setup:
- Setup you own .web credentials in the `secrets.yml` file.
- Specify/modify parameters in `ansible.cfg` (they should be similar if your python interpreter is at the same location as mine, if not just go on your unix terminal and run `which python` to see what/where your local install path is).
- Change inventory, `ansible-hosts` as you please, for the moment i'm using the `ios_command` module which sets up an ssh session within the module with no necessity to run anything on a separate ssh session so the inventory is a little irrelevant here.
- Change playbook variables to whatever desktop aggregation gateway / list of mac addresses of your liking :)

## How to Run:
```
ansible-playbook -i ansible-hosts playbook.yml -vvv
```

## Parsing:
- To learn more on how I've been doing the parsing make sure to explore the provided `textfsm` templates and `jinja2` templates, these are essential when diving deeper into Ansible and more specifically Ansible for Networking

## Results:
- Results are displayed and rendered as a csv: `report.csv`
- Feel free to mess around and try to print other things or use the `debug` module to explore more / get a better feel for registered variables and data format/structure parsing
