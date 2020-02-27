# Vagrant demo

With this vagrant repo, you install one ubuntu 18.04 bionic beaver machine. 

This repo is intended for educational purposes only. 

## Prerequisites

This setup is badly tested (: 

Works on MacOS Catalina.

Software needed:

- Vagrant 2.2.6 or higher
- virtualbox 5.0 or higher
- virtualbox extension pack

### MacOS Catalina

```bash
brew install vagrant
```

### Ubuntu 18.04

```bash 
apt install -y vagrant
```

### Windows 

Download url

```
https://www.vagrantup.com/downloads.html
```

## How start the Vagrant box

```
git clone https://github.com/moatn/vagrant01-demo
cd vagrant01-demo
vagrant up
```

```
$ vagrant ssh web01
```