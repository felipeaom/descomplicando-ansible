Deploy App v1
=========

Deploy App v1 para testar a estrutura provisionada em Kubernetes pelo Ansible.

Role
------------

Irá ser criado a estrutura de pastas, instalação do Nginx, arquivos de configurações e publicação da Aplicação.


Playbook Principal
----------------

main.yml

```
- hosts: k8s-master
  become: yes
  user: ubuntu
  roles:
  - {role: deploy-app, tags: ["deploy_app_role"]}
```
