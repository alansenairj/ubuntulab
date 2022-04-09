# ansible_docker_install - automação para a VM Vagrant que possui automação para instalação do docker e faz deploy de containers Portainer, Watchtower e Jenkins automaticamente. 

OBS - Portainer é um gerenciador de containers via interface web

# Playbook para automatizar a instalação do Docker em uma VM vagrant. 

Playbook simples, sem roles ou templates. 

- Salva o nome da versao e salva em uma varivel
- Ajusta o Timezone
- Gera Chave SSH
- Ajusta o Arquivo de Configuração do Ansible 
- Instala Pacotes da dependência do docker
- Adiciona a GPG key do Docker
- Adiciona o repositorio do Docker e usando a versão registrada
- Instala o Docker
- Adiciona o User docker ao grupo vagrant
- Inicia o Docker Service Daemon

Instruções para uso
Clonar o repositório, entrar no repositório extaído e executar "vagrant up" 
Entrar na VM usando "vagrant ssh"
Dica no Linux - instalar pacote unzip e digitar " unzip ansible_docker_install.zip

![image](https://user-images.githubusercontent.com/20565821/127348699-a5e7b5b5-8b8a-49ed-a427-5f7c5f19e203.png)
Para logar no container do Portainer, digitar no navegador: localhost:9000

