# OpenStack Kolla Deploy Steps

Update and Upgrade
```
apt update -y && apt upgrade -y
```

Install packge software
```
apt install htop iotop iftop python python-pip -y
```

Upgrade pip
```
sudo pip install --upgrade pip

pip install --upgrade --user pip
sudo cp /usr/local/bin/pip /usr/bin/ && sudo cp /usr/local/bin/pip2* /usr/bin/
```

Install ansible version 2.7.0
```
pip install ansible==2.7.0
ansible --version
```

Install kolla ansible
```
pip install kolla-ansible
```

Setup inventory kolla openstack ansible
```
cp -r /usr/local/share/kolla-ansible/etc_examples/kolla /etc/kolla/
cp /usr/local/share/kolla-ansible/ansible/inventory/all-in-one .
```

Configuration variable kolla ansible
```
grep -vE '^$|^#' /etc/kolla/globals.yml
vim /etc/kolla/globals.yml
grep -vE '^$|^#' /etc/kolla/globals.yml
```

Generate password for cluster
```
kolla-genpwd
```

Run bootstrap server
```
kolla-ansible -i all-in-one bootstrap-servers
docker --version
kolla-ansible pull
docker images
```
