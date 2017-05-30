### Sobre o Ansible
É uma ferramenta de automatização de tarefas semelhante a Puppet e Chef, porém muito mais poderosa e a queridinha do pessoal DevOps hoje. Com ela é possível fazer o deploy de aplicações, provisionando de servidores, automatizar tarefas, e outras funções.

O Ansible trabalha com arquivos YAML,  o principal arquivo de configuração é chamado de PLAYBOOK onde você coloca todas as tarefas que serão executadas “yum”,”mkdir”,”useradd” e no arquivo hosts você adiciona os servidores onde o Ansible irá executar esse PLAYBOOK. Cada Playbook possui roles que são as informações de provisionamento, após definir as roles você definirá em quais hosts essas roles serão executadas.

##### Instalando no CentOS
```bash
yum install ansible
```  
##### Exemplo de um arquivo hosts
```bash
[webservers]
192.168.33.10
192.168.33.11
```
##### Exemplo de um playbook webeservers.yaml
```bash
- hosts: webservers
  remote_user: root
  tasks:
  - name: Update YUM
    yum: name="*" state=latest
    
  - name: Install Nginx
    yum: name=nginx state=present
 ```
No exemplo acima criamos um playbook webserver.yaml para rodar em dois servidores que fara o papel de webserver o mesmo ira atualizar o S.O e instalar o Nginx.
