## Visão Geral do Projeto:

> _Este projeto tem como objetivo apresentar os conceitos fundamentais da virtualização. A partir da criação da minha primeira máquina virtual, utilizando o VirtualBox (ou UTM, caso o VirtualBox não seja uma opção), seguindo orientações específicas, o desafio é aprender a configurar e aplicar rigorosas regras de segurança no sistema operacional. Ao final, você será capaz de personalizar e administrar seu próprio sistema de maneira eficiente._

- Configuração de firewall com `UFW`
- Gerenciamento de permissões de administrador com `sudo`
- Implementação de políticas de segurança de senhas com `libpam-quality`
- Agendamento de tarefas de monitoramento com `cron`, executando scripts a cada 10 minutos

Além disso, o projeto abrange temas essenciais como criptografia, redes, particionamento de discos e programação de shell, com foco na formatação de saída de comandos!

---

### Comandos Comuns e Suas Funções

| Comando | Descrição |
| --- | --- |
| `lsblk` | Exibe as partições e dispositivos conectados |
| `sudo aa-status` | Mostra o status atual do *AppArmor* |
| `sudo ufw status verbose` | Verifica o status do serviço *ufw* (firewall) |
| `sudo ss -tunlp` | Verifica o status de conexões de rede, incluindo o serviço *ssh* |
| `hostnamectl status` | Exibe o nome do host e outras informações do sistema |
| `hostnamectl set-hostname <novo hostname>` | Altera o nome do host do sistema |
| `sudo awk -F ":" '{print $1}' /etc/passwd` | Lista todos os usuários cadastrados no sistema |
| `sudo awk -F ":" '{print $1}' /etc/group` | Exibe todos os grupos do sistema |
| `adduser <usuario>` | Cria um novo usuário com diretório home |
| `userdel -r <usuario>` | Remove um usuário e seu diretório home |
| `usermod -l <novo nome usuario> <usuario>` | Altera o nome de um usuário já existente |
| `groupadd <grupo>` | Cria um novo grupo de usuários |
| `groupdel <grupo>` | Exclui um grupo do sistema |
| `gpasswd -a <usuario> <grupo>` | Adiciona um usuário a um grupo específico |
| `gpasswd -d <usuario> <grupo>` | Remove um usuário de um grupo |
| `getent group <grupo>` | Exibe os usuários pertencentes a um grupo específico |
| `passwd <usuario>` | Modifica a senha de um usuário |
| `sudo visudo` | Permite editar o arquivo `/etc/sudoers` para configuração de permissões |
| `sudo ufw allow/deny <porta>` | Permite ou bloqueia acesso à porta especificada pelo *ufw* |
| `sudo ufw delete <linha>` | Remove uma regra específica do firewall |
| `ssh [usuario]@[ip da VM] -p [porta]` | Conecta-se à VM via SSH |
| `scp -P [porta] [arquivo] [usuario]@[ip da VM]:[diretorio]` | Copia arquivos para a VM usando SCP |
| `wall` ou `wall -n` | Exibe uma mensagem ou o conteúdo de um arquivo para todos os usuários conectados |
| `exit` ou `logout` | Finaliza a sessão do terminal conectado à VM |
| `sudo crontab -e` | Edita o arquivo de agendamento de tarefas `cron` |
