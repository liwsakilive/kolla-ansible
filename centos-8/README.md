Update package
```
dnf update -y
```
Install package
```
dnf install python3-devel libffi-devel gcc openssl-devel python3-libselinux
```
Install pip
```
dnf install python3-pip
```
Install ansible in pip
```
pip install 'ansible<3.0'
```
Install wheel
```
pip install wheel
```
Upgrade pip
```
pip install --upgrade pip
```
Install pip kolla-ansible
```
pip install kolla-ansible
```
Create the /etc/kolla directory
```
sudo mkdir -p /etc/kolla
sudo chown $USER:$USER /etc/kolla
``
Copy globals configuration and example inventory
```
cp -r kolla/share/kolla-ansible/etc_examples/kolla/* /etc/kolla
cp -r kolla/share/kolla-ansible/ansible/inventory/* .
```


