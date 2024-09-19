# Learnings

While executing Kelsey's tutorial, I needed to search the Internet for basics, and I'm collecting my learnings here to help other Hard Way enthusiasts close similar gaps in their knowledge.

## Repository

## Hardware

## Client Operating System

## Server Operating System

Like Kelsey, I chose a Debian-based release of Linux, [Ubuntu](https://ubuntu.com/download/desktop), to run on each machine, and as of this writing I'm running Ubuntu 24 Desktop. I will frequently upgrade my OS but not this doc, so I recommend you chose the current [LTS](https://ubuntu.com/about/release-cycle) version, whatever it may be.

### OS Version

Check the Ubuntu version you're running:
```bash
lsb_release -a
```

Check the CPU architecture:
```bash
uname -mov
```

### CPU Architecture


### OS Updates
```bash
sudo apt update
sudo apt upgrade
```

### ssh

Install ssh:
```bash
sudo apt install ssh
```

Enable ssh to survive reboot:
```bash
sudo systemctl enable ssh
```

Start ssh:
```bash
sudo systemctl start ssh
```

Allow ssh through the OS firewall and ensure the firewall is up:
```bash
sudo ufw allow ssh
sudo ufw enable
```

Check the status of ssh:
```bash
sudo systemctl status ssh
```

### Root

Set a password for the `root` user:
```bash
sudo passwd root
```

### Hostname

You may want to change your hostname from time to time as your cluster changes.

Use system control to change the hostname file for you:
```bash
sudo hostnamectl set-hostname linuxconfig
```

Replace any instance of the old host name in your hosts file:
```bash
sudo nano /etc/hosts
```
Press CTL-X to exit and confirm overwrite, then restart the machine.

## Networking

Get your IP address
```bash
hostname -I
```