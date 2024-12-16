  ## Project Summary:

> _This project aimed to introduce you to the wonderful world of virtualization. I created my first machine in VirtualBox (or UTM if you can't use VirtualBox)
> under specific instructions. So, by the end of this project, you will be able to configure your own operating system while implementing strict rules._

- setting up a firewall using `UFW`
- configuring system administration with `sudo`
- implementing strong password policy using `libpam-quality`
- setting up a `cron` task to run a monitoring script every 10 minutes
  
This project also covered the basics of criptography, networking, hard disk partitioning, and shell scripting (lots of output formatting!)

	
| Comando | Descrição |
| --- | --- |
| `lsblk` |  mostrar as partições |
| `sudo aa-status` | mostrar os status do *AppArmor* |
| `sudo ufw status verbose` |  check that the *ufw* service |
| `sudo ss -tunlp` |  check that the *ssh* service |
| `hostnamectl status` |  mostra o hostname atual e outras informações |
| `hostnamectl set-hostname <novo hostname>` |  alterar o hostname |
| `sudo awk -F ":" '{print $1}' /etc/passwd` |  mostra os *usuários* |
| `sudo awk -F ":" '{print $1}' /etc/group` |  mostra os *grupos* |
| `adduser <usuario>` |  cria um novo usuario com home e tudo |
| `userdel -r <usuario>` |  detela o usuario, -r deleta todos os arquivos |
| `usermod -l <novo nome usuario> <usuario>` |  muda o nome do usuario |
| `groupadd <grupo>` |  cria grupo |
| `groupdel <grupo>` |  deleta grupo |
| `gpasswd -a <usuario> <grupo>` |  adiciona o usuario no grupo |
| `gpasswd -d <usuario> <grupo>` |  remove o usuario do grupo |
| `getent group <grupo>` |  mostra usuarios que estão nesse grupo |
| `passwd <usuario>` |  trocar senha |
| `sudo visudo` |  entra para poder edita o arquivo /etc/sudoers |
| `sudo ufw allow/deny <porta>` | dar acesso/tirar acesso da porta |
| `sudo ufw delete <numero da linha a ser deletada>` |  deletar linha de acesso a alguma porta |
| `ssh [usuario logado]@[ip da VM] -p [porta x]` |  como conectar o terminal do seu computador com a VM |
| `scp -P [porta] [arquivo] [usuario logado]@[ip da VM]:[diretorio]` |  mandar arquivos do seu computador para a VM via terminal |
| `wall` ou `wall -n` |  exibe uma mensagem ou o conteudo de um arquivo no terminal de todos os usuarios conectados |
| `exit` ou `logout` |  terminar conexão do seu computador com a VM |
| `sudo crontab -e` |  editar o arquivo CRON |
