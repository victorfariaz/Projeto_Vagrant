# Projeto_Vagrant
Disciplina: Administração de Sistemas Abertos
Professor: Leonidas Lima
Período: 2025.2
Instituição: Instituto Federal da Paraíba - Campus João Pessoa

# 👥 Integrantes da Equipe
Victor 
MMiqueias

# 🎯 Objetivo
O projeto tem como objetivo desenvolver de uma infraestrutura virtual composta por 4 máquinas e a automatização da configuração de diversos serviços essenciais em ambiente Linux.

# 🖥️ Infraestrutura Virtual
Características Gerais
Provider: VirtualBox
Box: debian/bookworm64
Geração de chaves SSH desativada
Uso de clones (linked_clone)
Verificação de guest additions desabilitada
# Máquinas Virtuais
🔐 Servidor de Arquivos - arq
IP: 192.168.56.132
Hostname: arq.victor.devops
Discos adicionais: 3x10GB
Serviços: DHCP, LVM, NFS
🧮 Servidor de Banco de Dados - db
IP via DHCP
Hostname: db.victor.devops
Serviços: MariaDB, Autofs
🌐 Servidor de Aplicação - app
IP via DHCP
Hostname: app.victor.devops
Serviços: Apache2, Autofs
💻 Host Cliente - cli
IP via DHCP

Hostname: cli.victor.devops

Recursos: 1024MB RAM, Firefox, X11 Forwarding, Autofs

Como o Ansible não é executável diretamente no Windows, a VM arq foi utilizada como controladora para execução dos playbooks Ansible via SSH nas demais máquinas virtuais (db, app e cli).

