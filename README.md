# Ansible playbook for macOS

This playbook provides automatic installation of:

- Homebrew / Cask packages
- Font for terminal(Ricty)
- MacOS default system setting
- git
- zsh

on your macOS.

## Usage

### Setup

```sh
$ bash setup
```

Then you will be prompted like the following:

```sh
Copying your SSH public key into your clipboard...
Now you should add the generated key to GitHub before proceeding.
Are you sure you want to proceed? [Y/n] 
```

Your public key is already copied in your clipboard, so add the key to GitHub before hitting the enter key.

After all the setup processes are done, you will see the following message:

```sh
Initialization has been completed successfully.
To start provisioning, run

  $ cd /Users/XXX/ansible-mac
  $ GOPATH=~ ansible-playbook playbook.yml
```

Then go to the next step.
(If you encounter any problem during setup, fix it and re-run the script.)

### Full Installation

If you want to install all the packages above, just run

```sh
$ ansible-playbook playbook.yml
```

### Partial Installation

If you want to install a paticular package, for example, `homebrew`, run with `-t` option:

```sh
$ ansible-playbook playbook.yml -t homebrew
```

This provisions only Go environment.