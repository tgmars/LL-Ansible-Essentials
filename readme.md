# Running playbook
Because private keys for ansible connections are only copied across to the controller after the dev server is created and provisioned with cloud-init, we'll just use the `--private-key=` flag to specify it rather than going through a ssh-agent and ssh-add
`ansible-playbook -i inventory.ini -e file_state=touch first.yaml --private-key=/home/terraform/code/ansiblecontroller`