# Configurações pessoas básicas ao iniciar nova distro WSL (Ou em qualquer outro ambiente)

## Instruções gerais

```shell
## Instale o Ansible

## No Archlinux
sudo pacman -Syu ansible

## No Debian
sudo apt update && sudo apt install -y ansible

## Instale as dependências do Ansible
ansible-galaxy collection install -r requirements.yml

## Use o arquivo de variáveis de ambiente como exemplo e popule com seus dados
cp environment_vars.example.yml environment_vars.yml

## Execute o playbook
ansible-playbook -i hosts.ini playbook.yml --ask-become-pass

## Reinicie o terminal para aplicar as mudanças ou execute o comando abaixo
source ~/.bashrc 
```