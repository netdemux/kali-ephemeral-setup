<h1>kali-ephemeral-setup</h1>
Installs additional tools for Kali Linux. Used to quickly upgrade ephemeral instances of Kali for pentesting. Development aimed at Offsec Kali Desktop for Proving Grounds.

On the ephemeral Kali instance, install ansible:
```
sudo apt install ansible
```

Download the playbook and enter the directory:
```
git clone https://github.com/netdemux/kali-ephemeral-setup
cd kali-ephermeral-build
```

Install third party requirements:
```
ansible-galaxy install -r requirements.yml
```

Run the playbook:
```
ansible-playbook main.yml --ask-become-pass
```

*Note: run ansible as a user, then elevate, in order for ansible to access the correct environment variables and move configuration files into the user home directory.*
