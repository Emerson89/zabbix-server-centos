# Instalação zabbix-server usando ansible

## Dependências
- ansible 2.9.10
- CentOS Linux 7

## Edite o arquivo hosts para ip do host destino

## Exemplo de playbook
```
---
- name: Install Zabbix Server
  hosts: all
  become: yes
  roles:
  - zabbix-server
```
``` 
ansible-playbook -i hosts zabbix.yml
``` 