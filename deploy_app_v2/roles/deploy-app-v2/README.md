Deploy App v2
=========

Deploy App v2 para testar a estrutura provisionada em Kubernetes pelo Ansible.

Role
------------

Instalando dependencias, copiando arquivos do app v1, criando os arquivos do app v2 e criando a Aplicação.


Playbook Principal
----------------

main.yml

```
- hosts: k8s-master
  become: yes
  user: ubuntu
  roles:
  - {role: deploy-app-v2, tags: ["deploy_app_v2_role"]}
```
