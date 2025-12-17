<h1>kali-ephemeral-setup</h1>

<h2>Usage</h2>
Installs additional tools for Kali Linux. Used to quickly upgrade ephemeral instances of Kali for pentesting. Development aimed at Offsec Kali Desktop for Proving Grounds.  Based on IppSec's parrot-build repo and tutorial (https://github.com/IppSec/parrot-build).

<h2>Playbook Execution</h2>

On the ephemeral Kali instance, install ansible:
```
sudo apt install ansible
```

Download the repository and enter the new directory:
```
git clone https://github.com/netdemux/kali-ephemeral-setup && cd kali-ephermeral-build
```

Install third party requirements:
```
ansible-galaxy install -r requirements.yml
```

Run the playbook:
```
ansible-playbook main.yml --ask-become-pass
```

*Note: Run ansible as a user, then elevate, in order for ansible to access the correct environment variables referencing the user home directory. Running with sudo will install for root only (usually not intended).*
