# O Ansible
É uma ferramenta de automatização de tarefas semelhante a Puppet e Chef, porém muito mais poderosa e a queridinha do pessoal DevOps hoje. Com ela é possível fazer o deploy de aplicações, provisionando de servidores, automatizar tarefas, e outras funções.

O Ansible trabalha com arquivos YAML,  o principal arquivo de configuração é chamado de PLAYBOOK onde você coloca todas as tarefas que serão executadas “yum”,”mkdir”,”useradd” e no arquivo hosts você adiciona os servidores onde o Ansible irá executar esse PLAYBOOK. Cada Playbook possui roles que são as informações de provisionamento, após definir as roles você definirá em quais hosts essas roles serão executadas.
