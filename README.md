# Prerequisites

1. Install browser
2. Create SSH key https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
3. Add SSH key to GitHub
4. Install git
5. Clone this repo
6. Run `[repo]/setup.sh`
7. Ansible away!

# Usage

To setup the terminal env, run:

```sh
ansible-playbook ubuntu/terminal.yml
```

You can also overrdie the defaults by running:

```sh
ansible-playbook ubuntu/terminal.yml -e "ssh_key_path=[KEY_PATH]"
```

## Tags

Each tasks file comes with its own tag. So if you want to setup only vim and git: 

```sh
ansible-playbook ubuntu/terminal.yml --tags "vim,git"
```

You can also skip tags: 

```sh
ansible-playbook ubuntu/terminal.yml --skip-tags "vim,git"
```

System upgared is tagged with `always`, so if you want to omit it you need to explicitly skip it

```sh
ansible-playbook ubuntu/development.yml --skip-tags "always" --tags "elm"
```
