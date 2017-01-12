TI CONSULTING INFRASTRUCTURE
===

This repositoy contains the following tools:

  - Yii Framework
  - Mysql
  - NGINX

Usage
===

For new repos, clone including submodules.

```
  git clone --recursive https://github.com/Tinker-Ware/ticonsulting-infrastructure.git
```

For already cloned repos, just update the submodules.
```
  git submodule update --init --recursive
```

Modify your github credentials updating `provisioning/host_vars/ti.project1`

```
## GIT
gitconfig:
  user: user     ## ADD YOUR USER
  ssh: yes
  ssh_key_path: "/home/tinkerware/.ssh/ansible_id_rsa"
  option:
    user_email: user@ticonsulting.com  ## ADD YOUR GITHUB EMAIL
    user_name: username   ## ADD YOUR GITHUB USERNAME

```

If using a private repository, Include your private key in:
`provisioning/host_files/ti.project1/keys/private` in a file as follows:

```
priv_k: |
   << Private key here >>
```

Start working with the created Vagrant machine:
```
  vagrant up
```
When the process is done, you can view your project in your browser in: `192.168.33.10`

This will create a synced folder with your host machine `./tinker_share_files`.
All the files will be placed there ready to be modified.

HAPPY CODING!

FOR WINDOWS
===

**Run vagrant commands in a terminal with Administrator permissions**. (To be able to create symlinks)

Current DB Config
===

For development, de database is configured as it follows:

root password: rootpass
mysql user: "ticonsulting"
mysql host: "localhost" #Inside the Vagrant. or 192.168.33.10 from the outside.
mysql password: "password"
mysql database name: "ti_database"

For Database configurations and yii framework cookie validation key,
go to `provisioning/host_vars/ti.project1` if needed.

If any change is made, contact Tinkerware support. :)

Support
===

Please contact Tinkerware if any request or modification.

email: alfonso@tinkerware.io
Slack: tinkerware.slack.com
