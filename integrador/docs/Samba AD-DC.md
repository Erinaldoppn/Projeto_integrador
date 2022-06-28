### Instalação do Samba AD-DC

####Atualizar pacotes
   

 1. ` apt update `
 2. ` apt upgrade `
   
   
#### Configuração de IP nas interfaces de rede

1. `nano /etc/network/interfaces`

#### Nome da máquina

1. ` hostnamectl set-hostname escjsm `

#### configuração de Hosts

1. ` nano /etc/hosts`

#### Instalando servidor Samba

1. ` apt install samba krb5-user krb5-config winbind libpam-winbind libnss-winbind smbclien `

#### Parar e desabilitar o Serviço Samba(stop/disable)

1. `systemctl stop samba-ad-dc.service smbd.service nmbd.service winbind.service`
2. `systemctl disable samba-ad-dc.service smbd.service nmbd.service winbind.service`

#### Criando um backup do arquivo smb.conf

1. ` mv /etc/samba/smb.conf /etc/samba/smb.conf.bkp `

#### use-RCF2307

1. `samba-tool domain provision --use-rfc2307 --interactive`

#### Criando um backup do arquivo krb5.conf
1. ` mv /etc/krb5.conf /etc/krb5.conf.bkp `
2. `ln -s /var/lib/samba/private/krb5.conf /etc`

#### Desmascarar o serviço
1. `systemctl unmask samba-ad-dc.service`

#### Começar e Habilitar o serviço (star/enable)

1. `systemctl start samba-ad-dc.service`
2. `systemctl enable samba-ad-dc.service`

#### Level show domain
1. ` samba-tool domain level show `

## Compartilhamento de diretórios

1. Criando os diretórios coordenacão e professores.
2. Adicionando o grupo e incluindo aos diretórios específicos.
3. Alterando as permissões dos diretórios. 
4. Criando o usuário professor na máquina.
5. Criando o usuário coordenador na máquina.
6. Criando o usuário diretor na máquina.
7. Incluindo os usuários no grupo profissionais.
8. Criando e habilitando cada usuário no samba.
9. Criando o grupo profissionais no samba.
10. dicionando os usuários no grupo profissionais do samba.
11. Editando o arquivo “smb.conf” para a criação do compartilhamento
12. Reiniciando o serviço do samba
    1.  ` systemctl restart samba-ad-dc.service `

13. Mostrando os diretórios compartilhados

