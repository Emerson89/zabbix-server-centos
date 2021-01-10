# Instalação zabbix-server usando ansible

![Badge](https://img.shields.io/badge/ansible-zabbix-red)
![Badge](https://img.shields.io/badge/aws-zabbix-red)

## Dependências
![Badge](https://img.shields.io/badge/ansible-2.9.10-blue)
![Badge](https://img.shields.io/badge/CentOS-7-blue)

## Edite o arquivo hosts para ip do host destino, altere no arquivo zabbix.yml as senhas do GUI e BD de acordo com sua preferência

## Caso instale em OnPremisses use a v1.0

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
``` 
ansible-playbook -i hosts zabbix.yml
``` 
## Licença
![Badge](https://img.shields.io/badge/license-GPLv3-green)