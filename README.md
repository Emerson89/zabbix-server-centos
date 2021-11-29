# Instalação zabbix-server usando ansible

![Badge](https://img.shields.io/badge/ansible-zabbix-red)

## Dependências
![Badge](https://img.shields.io/badge/ansible-2.9.10-blue)
![Badge](https://img.shields.io/badge/CentOS-7-blue)

## Versões suportadas Zabbix-server
- 4.4 <= 
- 5.0 Versão Final

## Edite o arquivo hosts para ip do host destino

## Exemplo de playbook
```
---
- name: Install Zabbix Server
  hosts: all
  vars:
   pass_zabbix: CUSTOM_SENHA_ZABBIX
   zabbix_version: 4.4
  become: yes
  roles:
  - zabbix-server

ansible-playbook -i hosts zabbix.yml
```

## Licença
![Badge](https://img.shields.io/badge/license-GPLv3-green)