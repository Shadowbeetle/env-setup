# Prerequisites

1. Install browser
2. Log into GitHub
3. Create SSH key https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
4. Add SSH key to GitHub
5. Install git
6. Install pip `sudo apt-get -y install python3-pip python3-dev libffi-dev libssl-dev`
7. Install ansible `pip install ansible --user`

# Usage

To setup the terminal env, run:

```sh
ansible-playbook ubuntu/terminal.yml
```

You can also overrdie the defaults by running:

```sh
ansible-playbook ubuntu/terminal.yml -e "ssh_key_path=[KEY_PATH]"
```