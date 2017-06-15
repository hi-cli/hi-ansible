# hi-ansible: ansible hi-cli module

## Installation guide

1. Install [hi-cli](https://github.com/hi-cli/hi-cli)

2. Install hi-ansible package
```bash
hi package install ansible
```

3. Ansible Usages
```bash
hi ansible [ansible module] [host] [ansible arguments]
hi ansible shell all [any unix command]
```

4. Examples

* Run shell command 'free -h' on all remote hosts
```bash
hi ansible shell all free -h
```

* Run lineinfile to replace line of file /usr/lib/systemd/system/docker.service on all remote hosts
```bash
hi ansible lineinfile all dest=/usr/lib/systemd/system/docker.service regexp='Restart=.*$' line='Restart=always'
```