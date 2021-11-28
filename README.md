# Instalação zabbix-server 4.4 usando ansible

![Badge](https://img.shields.io/badge/ansible-zabbix-red)
![Badge](https://img.shields.io/badge/aws-zabbix-red)

## Dependências
![Badge](https://img.shields.io/badge/ansible-2.9.10-blue)
![Badge](https://img.shields.io/badge/CentOS-7-blue)

## Edite o arquivo hosts para ip do host destino, insira a senha do BD e do front

## Exemplo de playbook
```
---
- name: Install Zabbix Server
  hosts: all
  vars:
   pass_zabbix: CUSTOM_SENHA_ZABBIX
   zbx_database_password: CUSTOM_SENHA_ZABBIX_DB
  become: yes
  roles:
  - zabbix-server

ansible-playbook -i hosts zabbix.yml
```
mysql_root_users:
  - login_user: root
    login_password: "" 
    name: "{{ mysql_root_username }}"
    password: "{{ mysql_root_pass }}"
    host: "{{ zbx_user_privileges }}"
    priv: "*.*:ALL,GRANT"

## Licença
![Badge](https://img.shields.io/badge/license-GPLv3-green)